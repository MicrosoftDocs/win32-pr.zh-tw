---
description: Session 物件的 SetInstallLevel 方法會將目前安裝的安裝層級設定為指定的值，並重新計算功能資料表中所有功能的 [選取] 和 [已安裝] 狀態。
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: SetInstallLevel 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993241"
---
# <a name="sessionsetinstalllevel-method"></a>SetInstallLevel 方法

[**Session**](session-object.md)物件的 **SetInstallLevel** 方法會將目前安裝的安裝層級設定為指定的值，並重新計算功能資料表中所有功能的 [選取] 和 [已安裝] 狀態。 它也會根據新的層級，設定 [元件資料表](component-table.md) 中每個元件的動作狀態。

## <a name="syntax"></a>語法


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*installLevel* 
</dt> <dd>

需要新的安裝層級。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在呼叫 **SetInstallLevel** 之前，必須先執行 [CostInitialize 動作](costinitialize-action.md)。

如果為 *installLevel* 參數傳遞0，則不會變更目前的安裝層級，但仍會根據目前的安裝層級更新所有功能。 例如，處理常式模組可以使用這項功能，在 UI 選取程式中的任何時間點，將所有選取範圍重設回其初始預設狀態。

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




