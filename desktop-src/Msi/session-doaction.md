---
description: Session 物件的 Dataadapter.doaction 方法會執行對應至提供之名稱的動作函數。
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: 'Dataadapter.doaction 方法 (Photoacquire .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5c3f6451ec6ef920e6c6414a9396d2c4eeb2102ffc161e1ed91ce996752cd345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629388"
---
# <a name="sessiondoaction-method"></a>Dataadapter.doaction 方法

[**Session**](session-object.md)物件的 **dataadapter.doaction** 方法會執行對應至提供之名稱的動作函數。 如果提供 Null 動作名稱，引擎會使用 [action 屬性](action.md) 的大寫值做為要執行的動作。 如果未定義屬性值，則會執行預設動作，目前已定義為 [安裝]。 這個方法會傳回整數列舉。

## <a name="syntax"></a>語法


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*action* 
</dt> <dd>

要執行的動作所需的字串名稱。 區分大小寫。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

藉由呼叫 **dataadapter.doaction** 方法，無法執行更新系統的動作，例如 [InstallFiles](installfiles-action.md)和 [WriteRegistryValues](writeregistryvalues-action.md)動作。 這項規則的例外狀況是從 [InstallInitialize](installinitialize-action.md)和 [InstallFinalize 動作](installfinalize-action.md)之間 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中排程的自訂動作呼叫 **dataadapter.doaction** 方法。 您可以呼叫不會更新系統的動作，例如 [AppSearch](appsearch-action.md) 或 [CostInitialize](costinitialize-action.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| 標頭<br/>  | <dl> <dt>Photoacquire。h</dt> </dl>                                                                                                                                                               |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




