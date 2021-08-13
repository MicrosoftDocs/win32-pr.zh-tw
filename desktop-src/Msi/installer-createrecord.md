---
description: 安裝程式物件的 CreateRecord 方法會傳回具有所要求欄位數目的新記錄物件。
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: CreateRecord 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: da9c6132b79706cca2135ffcea1bff09040e15a90af5b8b3b1b7175a41229dc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631909"
---
# <a name="installercreaterecord-method"></a>CreateRecord 方法

[**安裝程式**](installer-object.md)物件的 **CreateRecord** 方法會傳回具有所要求欄位數目的新 [**記錄**](record-object.md)物件。

## <a name="syntax"></a>語法


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*計數* 
</dt> <dd>

需要的欄位數目，可能是0。 記錄中欄位的最大數目限制為65535。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

欄位0（而不是 *計數* 中的其中一個欄位）通常用於記錄導向的專案，例如格式字串或執行 op 程式碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




