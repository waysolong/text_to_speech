<!--
 * @Author: wuxulong19950206 1287173754@qq.com
 * @Date: 2024-03-12 21:51:41
 * @LastEditors: wuxulong19950206 1287173754@qq.com
 * @LastEditTime: 2024-03-12 21:55:25
 * @FilePath: \mandarin-tts-mtts\step.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
python wav2mel.py -c examples\biaobei\config.yaml -w examples\biaobei\Wave -m examples\biaobei\mel_folder

python prepare.py --wav_folder examples\biaobei\Wave --mel_folder examples\biaobei\mel_folder --generate_vocab True

python train.py -c examples\biaobei\config.yaml