---
description: ConfigureModule 物件是由用戶端所執行的介面。
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: 'ConfigureModule 物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7685ce1f1c9c7d8f519395c578000375742eea49dd169085e99c582e14c35a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143708"
---
# <a name="configuremodule-object"></a>ConfigureModule 物件

**ConfigureModule 物件** 是由用戶端所執行的介面。 Mergemod.dll在 **IMsmConfigureModule** 介面上呼叫方法，以要求用戶端工具提供設定資訊。 此模組會根據用戶端對此介面呼叫的回應進行設定。

## <a name="members"></a>成員

**ConfigureModule** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ConfigureModule** 物件有這些方法。



| 方法                                                           | 描述                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**ProvideIntegerData**](configuremodule-provideintegerdata.md) | 由 Mergemod.dll 呼叫以取得用來設定模組的整數。<br/> |
| [**ProvideTextData**](configuremodule-providetextdata.md)       | 由 Mergemod.dll 呼叫以取得用來設定模組的文字。<br/>     |



 

## <a name="remarks"></a>備註

### <a name="c"></a>C++

介面 **IMsmConfigureModule： IDispatch**

### <a name="interface-id"></a>介面識別碼



| 常數                     | 值                                  |
|------------------------------|----------------------------------------|
| **IID \_ IMsmConfigureModule** | {AC013209-18A7-4851-8A21-2353443D70A0} |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 2.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




