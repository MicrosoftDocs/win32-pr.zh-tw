---
description: UIPreview 物件的 ViewBillboard 方法會使用目前顯示之對話方塊中的主控制項來顯示撰寫的佈告欄。
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: UIPreview. ViewBillboard 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9892dc68ae5edb66759e4c19499af56d06fb6efac56b823821cd74c4a28644b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810368"
---
# <a name="uipreviewviewbillboard-method"></a>UIPreview. ViewBillboard 方法

[**UIPreview**](uipreview-object.md)物件的 **ViewBillboard** 方法會使用目前顯示之對話方塊中的主控制項來顯示撰寫的佈告欄。

## <a name="syntax"></a>語法


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*control* 
</dt> <dd>

裝載佈告欄、區分大小寫、以及控制項資料庫資料表之主鍵的控制項所需的名稱。

</dd> <dt>

*廣告 牌* 
</dt> <dd>

使用指定的控制項和目前的對話方塊，以及佈告欄資料庫資料表的主鍵，所要顯示的佈告欄的必要名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview 定義為 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




