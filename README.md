# UR5_초보자용
해당 저장소는 UR5(Universal Robotics 사) 로봇을 처음으로 입문하는 분을 위한 자료입니다.
This repository contains example code for getting started with the UR5 robot (Universal Robots).

여기서는 1) 키보드로 UR5를 조작하는 example, 2) UR5를 조작하여 춤을 추는 것처럼 보이게 하는 Dance task를 수행하는 example을 연습합니다. 

모든 예시에서는 항상 'ur5_rtde_bridge.py'파일을 터미널에서 먼저 수행하여, 노드 간의 통신이 가능하게 시작한 후 각 example을 수행하여야 합니다.
예를 들어, 2번 example의 경우 터미널에서 'ur5_rtde_bridge.py' 실행 -> 다른 터미널에서 'dance_master.py' 실행 -> 또 다른 터미널에서 'dancer.py'를 실행하여
3개의 터미널에서 각각의 파일을 실행하여 동작하도록 합니다.

(공통)
ur5_rtde_bridge.py : UR5 로봇과의 통신을 위한 파일로써 topic interface를 통해 다른 노드와 UR5를 연결해주는 파일. UR5 동작 시, 가장 처음으로 수행.
math_utils.py : rotation 등 관련 수학적 유틸리티들을 정의해놓은 파일.
ur5_saved_poses.json : 정해진 좌표에서 특정 동작을 수행할 수 있도록 pose의 좌표값들을 정의하는 파일.

(1번 task) teleop_keyboard.py : UR5를 키보드로 조작하기 위한 파일.
(2번 task)
dance_routines.yaml : dance라는 task를 수행하기 위해 motions를 정의하고, 정해진 motions를 routines에 따라 행동하여 dance라는 task를 수행한다.
dance_master.py : dance task 수행을 위해 dancer에게 topic으로 동작 명령을 보냄.
dancer.py : dance task 수행을 위한 main 파일


* 보다 나은 의견이나 수정사항이 있다면 언제든 환영합니다!
* Feel free to open an issue or submit a pull request if you have any suggestions or improvements!
