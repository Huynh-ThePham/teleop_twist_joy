# Teleop twist joy baseline

Upstream: https://github.com/ros2/teleop_twist_joy, tag 2.4.8 (head of `humble`),
commit d36ba5b7f6c394602bb147b4ce6609b554531f4b. The same version as the Humble deb
`ros-humble-teleop-twist-joy` 2.4.8 it replaces.

Built from source because the deb depends on the `joy` deb, which the source `joy`
(joystick_drivers fork) overrides: with the apt Nav2, joy and driver copies removed,
the deb would go with them and the gamepad would lose its teleop node.

No changes to the upstream code. `agv_base` `base.launch.py` starts `teleop_node`
with the Husky's PS4 mapping from its own parameters.
