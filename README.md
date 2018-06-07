# f110-vesc-docs
Documentation for setting up the F1/10 platform and the VESC speed controller.

<img src="images/cover_image.png" width="400">

# Necessary tools
Allen screwdriver

# Mechanical Setup
We will first assemble the car chassis and install the Jetson and power distribution board before setting up the VESC.

You should start with a Traxxas RC car with its chassis stripped away, as shown in the picture below. You car may already have some of the silver metal standoffs installed, but if it does not, we will go through the process of installing them. If you are ahead, you can jump to any point of this tutorial and pick up from there.

<img src="images/mech_barebones.jpg" width="400">

## Installing the Base Standoffs

Begin by installing three 45mm standoffs into the circled holes pictured below. Secure the standoffs to the car using three black 10mm Allen screws, with one screw per standoff. Pay attention to where you install the standoffs since there are several mounting holes on the car's base.

<img src="images/mech_base_screws_circled.jpg" width="400">
<img src="images/mech_base_allen_screws.jpg" width="400">
<img src="images/mech_base_screws_attached.jpg" width="400">

Next, install two threaded 14mm standoffs into the front holes in the car base. Don't mount the chassis to the car yet since we still need to mount the Jetson and power board to the chassis.

<img src="images/mech_base_front_screws_attached.jpg" width="400">

## Installing the Power Board, Jetson, and LIDAR Standoffs

Mount 4 standoffs to the black laser-cut chassis in the position shown below. Thread the provided 10mm Phillips head screws through the drill holes and screw them into the standoffs to secure them.

(**Important:** The chassis has a smooth, glossy side and a rougher side. Ensure the standoffs are mounted on the glossy side, with the screws on the rough side. Otherwise, the power board won't fit when you try to mount it.)

<img src="images/mech_power_screws_front.jpg" width="400">
<img src="images/mech_power_screws_back.jpg" width="400">

Do the same for the Jetson with four more 35mm standoffs, also mounted on the glossy side. For the Jetson, ensure the standoffs are mounted near the **left** cut-out oval on the chassis, not the right one.

<img src="images/mech_jetson_screws_front.jpg" width="400">

Mount two more (19mm) standoffs to the front part of the chassis for the LIDAR.

<img src="images/mech_lidar_screws_front.jpg" width="400">

## Mounting the Jetson and Power Board

Before mounting the power board to the chassis, attach two 25mm standoffs to the power board using Phillips screws. (The mounting holes for the standoffs are located near the long headers for the Teensy.)

<img src="images/mech_power_board_antenna_standoffs.jpg" width="400">

Once you've done this, attach the Jetson Wi-Fi antenna to the standoffs using two more Phillips screws. Ensure that the antenna is mounted towards the board so that when the antennas are extended, they extend over the board and not away from it. See the picture below for clarification.

<img src="images/mech_power_board_antenna_screws.jpg" width="400">

Attach the two wires for the Jetson Wi-Fi antenna to the two gold-colored connectors near the fan connector on the heat sink. This can be a little tricky, so you might want to use a flathead screwdriver to ensure the connections are tight.

<img src="images/mech_antenna_disconnected.jpg" width="400">
<img src="images/mech_antenna_connected.jpg" width="400">

Cut two short (~6 inch) pieces of wire, preferably of different colors, and strip the ends to a short length (1/8 to 1/4 inch) Locate the green terminal block on the Jetson and attach one wire to the `+Vin` terminal, and another to one of the `12V` terminals on the power board. Connect the other stripped wire to the `GND` terminal on the Jetson and the `GND` terminal on the power board corresponding to the `12V` connection you made earlier. Use a small flathead screwdriver to secure the wires in place.

<img src="images/mech_jetson_power_wires_stripped.jpg" width="400">
<img src="images/mech_jetson_power_wires_connected.jpg" width="400">

Screw both the Jetson and the power board onto the chassis. The Jetson should be secured using longer (20mm) Phillips screws, while the power board should be secured using 10mm screws. Note that the Jetson also comes with four white plastic standoffs; these should be placed between the Jetson PCB and heatsink before threading the screws through. Ensure that the wires for neither the Wi-Fi antenna nor the Jetson's power connections get pinched. It might help to tuck both sets of wires underneath the power board. (Don't tuck them underneath the Jetson because they might restrict airflow or obstruct the fan's blades.)

<img src="images/mech_jetson_power_board_mounted.jpg" width="400">

Don't mount the LIDAR yet. We will do this after mounting the chassis to the car. (The LIDAR is very expensive, and we don't want to risk it getting damaged when mounting the chassis.)

## Mounting the Chassis to the Car

Place the chassis onto the five standoffs on the car base and align the chassis drill holes with the standoffs you attached earlier. Use five 10mm Phillips screws to secure the chassis to the standoffs. Your car should now look like the one in the image below:

<img src="images/mech_chassis_mounted.jpg" width="400">

## Mounting the LIDAR to the Chassis

Check to make sure you have the following parts for mounting the LIDAR:
- Three 3D-printed plastic mounts. One of these should be black and look similar to a tree, and the two others should be white C-shaped brackets.
- Two 10mm Phillips screws
- Hokuyo LIDAR

The parts are also shown in the image below.

<img src="images/mech_lidar_parts.jpg" width="400">

The LIDAR should have two cords: one for power and another for either Ethernet or USB. Cut the end of the power cord, leaving 1-2 feet of cable. Strip the end, cut away all wires except for the blue and brown ones, and strip those two wires to 1/8 inch.

Mount the white brackets to the black tree-shaped base as shown in the pictures below.

<img src="images/mech_lidar_brackets_back.jpg" width="400">

Attach the LIDAR to the rough side of the base using the two screws. Note: The base has four screw holes and the LIDAR only has two; just attach the two screws where the holes in the LIDAR are.

<img src="images/mech_lidar_brackets_front.jpg" width="400">

Locate the two mounting holes on the front of the car near the front bumper. Mount the LIDAR by fitting the two protruding parts of the white mounting brackets into the holes. The open part of the "C" in the brackets should face forward as shown below. If done correctly, two of the holes on the LIDAR base should match up with the two 19mm standoffs you mounted earlier. Secure the base to these standoffd using two 10mm Phillips screws.

<img src="images/mech_lidar_bumper_holes.jpg" width="400">
<img src="images/mech_lidar_mounted.jpg" width="400">
<img src="images/mech_lidar_secured.jpg" width="400">

Attach the LIDAR's power cable to a free 12V terminal block on the power board. The brown wire should go to the `12V` terminal, and the blue wire should go to the corresponding `GND` terminal. The side of the LIDAR has a pinout as well if you get confused.

<img src="images/mech_lidar_power_connection.jpg" width="400">

If the LIDAR has an Ethernet cable, attach it to the Ethernet port on the Jetson. If it has a USB cable, plug it into the USB hub.

<img src="images/mech_lidar_ethernet.jpg" width="400">

**Optional:** If you plan on using a USB keyboard and mouse for the Jetson and have a small (less than 5 port) USB hub, plug another USB hub into the first one.

<img src="images/mech_extra_usb_hub.jpg" width="400">

Plug the cord of the USB hub into the USB port on the Jetson. If your hub has power buttons, ensure all of them are set to the ON position. At this point, your car should be assembled, sans VESC.

# VESC Connections
Make sure you have the following items:
- Traxxas RC Car. This should also come with a servo motor (for steering) and a motor for driving the wheels. You'll need to connect both motors to the VESC later.
- VESC 4 electronic speed controller
- Traxxas 11.1v LIPO or 8.4v NiMH battery
- Battery connector (splitter)
- Power distribution PCB
- Mini USB cable
- USB hub

<img src="images/hw_overview.jpg" width="400">

Begin by connecting the drive motor to the VESC. The motor has three color-coded connections that correspond with connections on the VESC.

<img src="images/hw_vesc_drive_motor.jpg" width="400">

Next, connect the steering servo motor to the three-pin unshrouded male header on the VESC. Pay attention to the orientation of the servo connector since it is possible (and quite easy!) to plug the servo in backwards. If the VESC is oriented with the three-pin header at the top left, as pictured, the black wire should go on the left, the red in the middle, and the white on the right.

<img src="images/hw_vesc_servo_motor.jpg" width="400">

Plug the USB cable into the USB port of the VESC. Pull the other end of this cable through the oval-shaped cutout on the top right of the car chassis, and plug this into the USB hub. Plug the USB hub into the Jetson on the car if it is not already connected.

<img src="images/hw_vesc_usb_mini.jpg" width="400">
<img src="images/hw_vesc_usb_pull.jpg" width="400">
<img src="images/hw_vesc_usb_hub.jpg" width="400">

The VESC should now be on the right side of the chassis. Pull the 2-pin VESC battery connector through the chassis from the right side to the left side, and tuck the VESC in the right side of the car between the bottom of the car and the laser-cut chassis.

<img src="images/hw_vesc_battery_push.jpg" width="400">
<img src="images/hw_vesc_battery_pull.jpg" width="400">
<img src="images/hw_vesc_mount.jpg" width="400">

Connect the VESC battery connector to the battery splitter, and connect the white 4-pin header on the battery splitter to the corresponding header on the power distribution PCB. Ensure that the large silver toggle switches `U$3`, `U$4`, and `U$5` on the power board are OFF (toggled towards the white battery header).

<img src="images/hw_connect_splitter_vesc.jpg" width="400">
<img src="images/hw_connect_splitter_power_board.jpg" width="400">
<img src="images/hw_connect_splitter_battery.jpg" width="400">

Plug the battery into the remaining end of the splitter, and tuck the battery into the left side of the chassis.

<img src="images/hw_battery_mount.jpg" width="400">

At this point, the hardware should be set up. Your car should look similar to the one below.

<img src="images/final_assembled_car.jpg" width="400">

# Tips for Cable Management

Place the primary hub under the power board and route all USB cables behind the standoff next to the Teensy headers. (If you used another hub for keyboard and mouse, don't worry about securing it; you can disconnect it before driving the car.) Using shorter USB cables may help.

For the VESC, make sure the motor wires are on the right side of the car and are not touching the rod for the drivetrain. If you have room on the left side, you can place the USB cable for the VESC above the battery. All of the cables should be able to fit between the car chassis and base.

It's a good idea to use cable or zip ties to secure some of the longer wires, such as the LIDAR power and Ethernet cords and USB cables. You may want to tuck the cables for the LIDAR underneath the chassis through the oval-shaped cutout on the left side of the chassis. Wrapping the cables around the base of the LIDAR might also work.

Below is an example of how you might want to organize the cables.

<img src="images/mech_cable_management_right.jpg" width="400">
<img src="images/mech_cable_management_left.jpg" width="400">
<img src="images/mech_cable_management_lidar.jpg" width="400">
