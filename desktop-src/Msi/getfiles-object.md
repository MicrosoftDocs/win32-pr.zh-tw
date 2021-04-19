---
description: GetFiles 物件會抓取模組特定語言所需的檔案。 需要透過 Merge 物件執行某些動作，此介面的所有部分才會傳回有效的結果。
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: 'GetFiles 物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984862"
---
# <a name="getfiles-object"></a>GetFiles 物件

**GetFiles** 物件會抓取模組特定語言所需的檔案。 需要透過 [Merge 物件](merge-object.md) 執行某些動作，此介面的所有部分才會傳回有效的結果。

## <a name="members"></a>成員

**GetFiles** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**GetFiles** 物件具有這些屬性。



| 屬性                                               | 描述                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ModuleFiles**](getfiles-modulefiles.md)<br/> | [**ModuleFiles**](getfiles-modulefiles.md) 屬性會傳回目前開啟之模組的檔案 [資料表](file-table.md) 的所有主鍵。<br/> |



 

## <a name="c"></a>C++

介面 **IMsmGetFiles： IDispatch**

## <a name="interface-id"></a>介面識別碼



| 常數              | 值                                  |
|-----------------------|----------------------------------------|
| **IID \_ IMsmGetFiles** | {7041AE26-2D78-11D2-888A-00A0C981B015} |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




