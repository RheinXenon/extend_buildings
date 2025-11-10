# 居民署建筑扩展 (Resident Office Building Mod)

## 简介
这个mod为《欧陆风云5》添加了居民署建筑，为已有一定规模的聚居地提供基础行政管理服务。

## 建筑特性
- **名称**: 居民署 (Resident Office)
- **类型**: 基础设施建筑
- **最大等级**: 1级
- **人口类型**: 农民 (peasants)
- **建造时间**: 村庄建造时间
- **适用地点**: 农村定居点、城镇、城市

## 建造条件
- 地区人口比例 < 60%
- 当地区人口比例超过60%时自动移除

## 效果
- 本地人口增长: +0.01 (+1%)

## 安装方法

### 本地开发模式（推荐）
1. 将整个 `extend_buildings` 文件夹复制到：
   ```
   Documents/Paradox Interactive/Europa Universalis V/mod/
   ```

2. 启动游戏，在mod管理器中启用此mod

### 当前位置（仅供测试）
当前mod位于游戏安装目录下，这不是推荐的使用位置，因为游戏更新可能会覆盖这些文件。

## 开发调试

### 启用调试模式
在Steam中右键游戏 -> 属性 -> 启动选项，添加：
```
-debug_mode
```

### 查看错误日志
错误日志位置：
```
Documents/Paradox Interactive/Europa Universalis V/logs/error.log
```

## 文件结构
```
extend_buildings/
├── .metadata/
│   └── metadata.json          # Mod元数据（必需）
├── in_game/                   # 游戏内容顶层目录（必需）
│   ├── common/
│   │   └── building_types/
│   │       └── resident_office.txt
│   ├── gfx/
│   │   └── interface/
│   │       └── icons/
│   │           └── buildings/
│   │               └── resident_office.dds
│   └── localization/
│       └── simp_chinese/
│           └── resident_office_l_simp_chinese.yml
├── README.md                  # 本文件
└── 修改说明.md               # 结构修正详细说明
```

## 技术说明

### 生产方法
建筑使用 `colony_maintenance` 作为维护方法。如果游戏中不存在这个生产方法ID，你需要：
1. 在 `in_game/common/production_methods/` 下创建定义文件
2. 或者在建筑定义中直接指定资源输入输出

### 兼容性
- 支持游戏版本: 1.0.*（所有1.0.x版本）
- 不覆盖任何原版文件
- 使用独立的建筑ID，不应与其他mod冲突

## 已知问题
无

## 版本历史
- **v1.0.0** (2025-11-10)
  - 初始版本
  - 添加居民署建筑
  - 修正mod目录结构符合官方规范

## 许可证
此mod可自由使用和修改。

## 反馈
如有问题或建议，请检查error.log文件中的错误信息。

## 参考资源
- [EU5 Mod Structure Wiki](官方维基链接)
- [EU5 Modding Wiki](官方维基链接)

