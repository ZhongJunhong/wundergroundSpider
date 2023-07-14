wundergroundSpider.py：cleanData模块用与清洗数据

data.csv：wunderground爬虫数据

error.txt：因网络问题没有成功获取的数据

append_data.csv：对data数据的补充，因网络问题部分地区没有爬到

zbaa_v2.csv：使用cleanData模块清洗后的数据，包括：
 - 温度，华氏度转为摄氏度
 - 时间，从gmt timestrap转为东八区时间【重要】
 - 计算连续变量日均值、日最大、最小值
 - 对类型变量计算当日出现最多的值，尤其是风向，虽然是64位浮点类型，但也是按照类型变量计算的
 - 根据紫外线指数，计算当日日照时长

requirements.txt: 需要安装的依赖包
终端运行以下命令:
conda create --name wundergroundSpider --file requirements.txt -y
conda activate wundergroundSpider