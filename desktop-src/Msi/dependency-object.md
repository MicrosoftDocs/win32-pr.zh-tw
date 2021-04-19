---
description: 相依性物件會傳回目前模組相依的模組，而該模組尚未合併到目前的安裝資料庫中。
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: 'Dependency 物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992941"
---
# <a name="dependency-object"></a>Dependency 物件

相依 **性物件會** 傳回目前模組相依的模組，而該模組尚未合併到目前的安裝資料庫中。

## <a name="members"></a>成員

相依 **性物件具有** 下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

相依 **性物件具有** 這些屬性。



| 屬性                                           | 描述                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**語言**](dependency-language.md)<br/> | 傳回模組的語言。<br/>           |
| [**模組**](dependency-module.md)<br/>     | 傳回所需模組的模組識別碼。<br/> |
| [**版本**](dependency-version.md)<br/>   | 傳回所需模組的版本。<br/>   |



 

## <a name="c"></a>C++

介面 **IMsmDependency： IDispatch**

## <a name="interface-id"></a>介面識別碼



| 常數                | 值                                  |
|-------------------------|----------------------------------------|
| **IID \_ IMsmDependency** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




