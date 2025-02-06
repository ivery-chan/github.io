from psychopy import visual, core, event, data, gui
import random
import os

# 预先储存30个参与者的名字列表
all_participant_names = ['Chan Lai Yin', 'Chan Yiu Sum', 'Cheng Chung Yiu', 'Chen Nan Xiang', 'Choi Tsz Kin', 'Fung Ka Him', 'Hui Yiu Hei', 'Hung Siu Lun', 'Julian Miu', 'Kwong Tsz Lok', 
                         'Lai Man Lok', 'Lam Kwan Yiu', 'Law Orion', 'Leung Chun Ho', 'Leung Tak Hong', 'Leung Tik Fung', 'Li Wing Sang', 'Lin Bo', 'Lin Jing Sheng', 'Lo Wai Hei', 
                         'Liao Wen Wu', 'Shek Ho Nam', 'Thapa Prabin', 'Tso Chun Yu', 'Wong Chun Kit', 'Wong Ho Yin', 'Wong Yuen Cheong', 'Wong Zan Kwan', 'Yeung Tat Hong', 'Zhao Zi Feng']

# 储存参与者照片的字典，键是名字，值是对应的照片路径
all_participant_faces = {}
for name in all_participant_names:
    face_path = f'{name}_face.png'
    all_participant_faces[name] = face_path

# 设置对话框以收集参与者信息
expInfo = {'Participant': ''}
dlg = gui.DlgFromDict(dictionary=expInfo, title='ANT Experiment')
if not dlg.OK:
    core.quit()

# 获取参与者的名字和照片
self_name = expInfo['Participant']
self_face_path = all_participant_faces.get(self_name)

if self_face_path is None:
    print(f"Error: The name {self_name} is not in the stored participant list.")
    core.quit()

# 非自我相关的名字列表
other_names = [name for name in all_participant_names if name != self_name]

# 创建窗口和刺激
win = visual.Window([1200, 800], color='grey', units='pix')

# 固定十字
fixation = visual.TextStim(win, text='+', color='black', height=60)

# 加载参与者的照片
try:
    self_face = visual.ImageStim(win, image=self_face_path, size=(150, 150))
except Exception as e:
    print(f"Error loading participant's face image. {e}")
    core.quit()

# 加载其他人的照片
other_faces = []
for name in other_names:
    try:
        other_face_path = all_participant_faces[name]
        other_face = visual.ImageStim(win, image=other_face_path, size=(150, 150))
        other_faces.append((name, other_face))
    except Exception as e:
        print(f"Error loading {name}'s face image. {e}")
        core.quit()

# Cue 显示文本
cue_stim = visual.TextStim(win, text='', color='black', height=60)

# 创建响应键：a 是识别自己，l 是识别他人
response_keys = ['a', 'l']

conditions = [
    # Self-related information
    {'self_info': 'self', 'cue': 'noCue', 'flanker': 'congruent'},
    {'self_info': 'self', 'cue': 'centerCue_valid', 'flanker': 'congruent'},
    {'self_info': 'self', 'cue': 'centerCue_invalid', 'flanker': 'congruent'},
    {'self_info': 'self', 'cue': 'doubleCue_valid', 'flanker': 'congruent'},
    {'self_info': 'self', 'cue': 'doubleCue_invalid', 'flanker': 'congruent'},
    {'self_info': 'self', 'cue': 'spatialCue_valid', 'flanker': 'congruent'},
    {'self_info': 'self', 'cue': 'spatialCue_invalid', 'flanker': 'congruent'},
    {'self_info': 'self', 'cue': 'noCue', 'flanker': 'incongruent'},
    {'self_info': 'self', 'cue': 'centerCue_valid', 'flanker': 'incongruent'},
    {'self_info': 'self', 'cue': 'centerCue_invalid', 'flanker': 'incongruent'},
    {'self_info': 'self', 'cue': 'doubleCue_valid', 'flanker': 'incongruent'},
    {'self_info': 'self', 'cue': 'doubleCue_invalid', 'flanker': 'incongruent'},
    {'self_info': 'self', 'cue': 'spatialCue_valid', 'flanker': 'incongruent'},
    {'self_info': 'self', 'cue': 'spatialCue_invalid', 'flanker': 'incongruent'},

    # Non-self-related information
    {'self_info': 'non_self', 'cue': 'noCue', 'flanker': 'congruent'},
    {'self_info': 'non_self', 'cue': 'centerCue_valid', 'flanker': 'congruent'},
    {'self_info': 'non_self', 'cue': 'centerCue_invalid', 'flanker': 'congruent'},
    {'self_info': 'non_self', 'cue': 'doubleCue_valid', 'flanker': 'congruent'},
    {'self_info': 'non_self', 'cue': 'doubleCue_invalid', 'flanker': 'congruent'},
    {'self_info': 'non_self', 'cue': 'spatialCue_valid', 'flanker': 'congruent'},
    {'self_info': 'non_self', 'cue': 'spatialCue_invalid', 'flanker': 'congruent'},
    {'self_info': 'non_self', 'cue': 'noCue', 'flanker': 'incongruent'},
    {'self_info': 'non_self', 'cue': 'centerCue_valid', 'flanker': 'incongruent'},
    {'self_info': 'non_self', 'cue': 'centerCue_invalid', 'flanker': 'incongruent'},
    {'self_info': 'non_self', 'cue': 'doubleCue_valid', 'flanker': 'incongruent'},
    {'self_info': 'non_self', 'cue': 'doubleCue_invalid', 'flanker': 'incongruent'},
    {'self_info': 'non_self', 'cue': 'spatialCue_valid', 'flanker': 'incongruent'},
    {'self_info': 'non_self', 'cue': 'spatialCue_invalid', 'flanker': 'incongruent'}
]

# Shuffle the conditions and select 56 for the experiment (each condition appears twice)
selected_conditions = conditions * 2  # Duplicate the conditions list to have two of each
random.shuffle(selected_conditions)  # Shuffle to randomize the order

# Create a TrialHandler to run the selected conditions (56 trials total)
trials = data.TrialHandler(selected_conditions, nReps=1, method='random', extraInfo=expInfo)

# Add a function to determine if the response is correct
def is_correct_response(self_info, key_pressed):
    if self_info == 'self' and key_pressed == 'a':
        return True  # Correct if the central picture is self-related and 'a' is pressed
    elif self_info == 'non_self' and key_pressed == 'l':
        return True  # Correct if the central picture is non-self-related and 'l' is pressed
    return False  # Any other case is incorrect

# Present a single trial and implement the correct timing flow
def present_trial(self_info, cue_type, flanker_type):
    # 随机选择固定十字的持续时间（400-1600ms）
    initial_fixation_duration = random.uniform(0.4, 1.6)
    fixation.draw()
    win.flip()
    core.wait(initial_fixation_duration)

# Initialize variables to store the cue name and flanker names
    cue_name = ''
    flanker_names = []


    # 显示 Cue 100ms
    if cue_type == 'noCue':
        cue_stim.text = ''
        cue_name = 'noCue'
    elif cue_type == 'centerCue_valid':
        cue_name = self_name  # Self-related valid cue
        cue_stim.text = self_name
        cue_stim.pos = (0, 0)
    elif cue_type == 'centerCue_invalid':
        cue_name = random.choice(other_names)  # Non-self-related invalid cue
        cue_stim.text = cue_name
        cue_stim.pos = (0, 0)
    elif cue_type == 'doubleCue_valid':
        cue_name = self_name  # Self-related valid double cue
        cue_stim.text = self_name
        cue_stim.pos = (0, 250)  # Top position
        cue_stim.draw()
        cue_stim.pos = (0, -250)  # Bottom position
    elif cue_type == 'doubleCue_invalid':
        cue_name = random.choice(other_names)  # Non-self-related invalid double cue
        cue_stim.text = cue_name
        cue_stim.pos = (0, 250)  # Top position
        cue_stim.draw()
        cue_stim.pos = (0, -250)  # Bottom position
    elif cue_type in ['spatialCue_valid', 'spatialCue_invalid']:
        cue_name = random.choice([self_name] + other_names)
        cue_stim.text = cue_name
        # Set the position based on self-related or non-self-related condition
        if self_info == 'self':
            cue_stim.pos = (-250, 0)  # Always left for self-related condition
        else:
            cue_stim.pos = (250, 0)  # Always right for non-self-related condition


    # Draw the cue for 100 ms
    cue_stim.draw()
    win.flip()
    core.wait(0.2)  # Cue 显示 100ms

    # 显示后续 400ms 的固定十字
    fixation.draw()
    win.flip()
    core.wait(0.4)

    # 随机选择图像显示的位置（200像素上下偏移）
    y_position = random.choice([250, -250])  # 200 pixels above or 200 pixels below

    # 显示目标和干扰物（5 张图片），直到参与者响应或达到1700ms
    central_target = self_face if self_info == 'self' else random.choice(other_faces)[1]
    central_name = self_name if self_info == 'self' else random.choice(other_names)
    
    if flanker_type == 'congruent':
        flankers = [central_target] * 5  # 中央目标和两侧干扰物一致
        flanker_names = [central_name] * 5  # All flankers are the same
    else:
        chosen_other_face = random.choice(other_faces)[1]
        chosen_other_name = random.choice(other_names)
        flankers = [chosen_other_face, chosen_other_face, central_target, chosen_other_face, chosen_other_face]
        flanker_names = [chosen_other_name, chosen_other_name, central_name, chosen_other_name, chosen_other_name]

    # Set positions so that there is equal spacing between images
    spacing = 200  # You can adjust this value based on your display and aesthetics
    positions = [-2*spacing, -spacing, 0, spacing, 2*spacing]  # X-axis positions for flankers
    for i, f in enumerate(flankers):
        f.pos = (positions[i], y_position)  # Set the y_position either above or below
        f.draw()
    
    # Flip to display target and flankers
    win.flip()

    # 启动反应时间计时器 (开始记录时间从显示图片开始)
    response_timer = core.Clock()  # Start RT clock after images appear
    response = event.waitKeys(maxWait=1.7, keyList=response_keys, timeStamped=response_timer)  # RT measured from this point

    # 记录反应时间和按键
    if response:
        rt = response[0][1]  # The RT is now correctly measured from the moment the images appear
        key_pressed = response[0][0]
        trials.addData('rt', rt)  # 记录反应时间
        trials.addData('key', key_pressed)  # 记录按键 ('a' 或 'l')

        # Check if the response is correct based on the central target (self or non_self)
        correct = is_correct_response(self_info, key_pressed)
        trials.addData('correct', correct)  # Store whether the response was correct (CR)
    else:
        rt = 1.7  # If no response, use the maximum reaction time
        trials.addData('rt', None)
        trials.addData('key', None)
        trials.addData('correct', False)  # No response is considered incorrect
        trials.addData('missed', True)  # Mark this trial as missed
        print("No response recorded. Trial marked as missed.")

    # Save additional data about the cue and flanker names
    trials.addData('cue_name', cue_name)  # Store the name shown in the cue
    trials.addData('flanker_names', flanker_names)  # Store the names of flankers

    # Post-target fixation period: 3500ms - initial fixation duration - RT
    post_target_duration = 3.5 - initial_fixation_duration - rt

    # If there's remaining time in the trial, show the fixation cross
    if post_target_duration > 0:
        fixation.draw()
        win.flip()
        core.wait(post_target_duration)
    else:
        print("Reaction time or fixation time exceeded the total trial time.")

# 主实验循环：运行 30 次实验
for trial in trials:
    present_trial(trial['self_info'], trial['cue'], trial['flanker'])

# 导出为 HTML 时的数据保存逻辑
import json
data_to_save = []
for thisTrial in trials:
    trial_data = {
        'self_info': thisTrial['self_info'],
        'cue': thisTrial['cue'],
        'flanker': thisTrial['flanker'],
        'rt': thisTrial['rt'],
        'key': thisTrial['key'],
        'correct': thisTrial['correct'],
        'cue_name': thisTrial['cue_name'],
        'flanker_names': thisTrial['flanker_names']
    }
    data_to_save.append(trial_data)

# 保存为 JSON 格式
json_data = json.dumps(data_to_save, indent=4)

# 在 PsychoPy 导出为 HTML 时，这里的数据将通过 JavaScript 保存
# 以下是提示参与者下载数据的伪代码
from psychopy import visual, event
win = visual.Window(size=(800, 600), units='pix')
message = visual.TextStim(win, text='实验已结束，请点击下面的链接下载数据文件。', pos=(0, 0))
message.draw()
win.flip()
event.waitKeys()
win.close()