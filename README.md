# 居民署建筑扩展 (Resident Office Building Mod)

## 简介

为《欧陆风云5》添加居民署建筑，提供基础行政管理服务，支持三种生产方式调节人口增长。

## 建筑特性

- **建造条件**: 地区人口比例 < 60%
- **基础效果**: +0.1% 人口增长
- **类型**: 基础设施建筑（1级，农民工作）

## 生产方式对比

| 生产方式               | 资源消耗                    | 额外效果               | 总人口增长     |
| ---------------------- | --------------------------- | ---------------------- | -------------- |
| **基础居民服务** | 木材0.1, 工具0.1, 布料0.1   | +0.4%增长              | **0.5%** |
| **改进居民服务** | 木材0.1, 工具0.2, 布料0.15  | +0.6%增长, +5%疾病抗性 | **0.7%** |
| **高级人口管理** | 木材0.15, 工具0.3, 布料0.25 | +0.9%增长, +8%疾病抗性 | **1.0%** |

## 安装方法

1. 复制 `extend_buildings` 文件夹到：
   ```
   Documents/Paradox Interactive/Europa Universalis V/mod/
   ```
2. 在游戏mod管理器中启用

## 重要技术说明

### 生产方式modifier验证

⚠️ **关键测试点**: 游戏原版未见生产方式使用modifier的先例，需验证是否生效：

- **如果生效**: 三种方式提供0.5%、0.7%、1.0%不同增长
- **如果不生效**: 所有方式均为0.1%基础增长，仅资源消耗有差异

### 测试步骤

1. 建造居民署，切换不同生产方式
2. 记录人口增长率和疾病抗性数值
3. 检查 `Documents/Paradox Interactive/Europa Universalis V/logs/error.log`

### 文件结构

```
extend_buildings/
├── in_game/common/
│   ├── building_types/resident_office.txt
│   └── production_methods/resident_office_production_methods.txt
└── main_menu/localization/
    ├── english/resident_office_l_english.yml
    └── simp_chinese/resident_office_l_simp_chinese.yml
```

## 版本历史

- **v2.0.0** (2025-11-10) - 添加三种生产方式系统
- **v1.0.1** (2025-11-10) - 修复本地化UTF-8 with BOM编码
- **v1.0.0** (2025-11-10) - 初始版本

## 兼容性

- 游戏版本: 1.0.*
- 不覆盖原版文件
- 本地化: UTF-8 with BOM编码
