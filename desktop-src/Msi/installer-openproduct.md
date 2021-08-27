---
description: 安裝程式物件的 OpenProduct 方法會使用產品代碼開啟已安裝產品的安裝程式套件，並傳回會話物件。
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: OpenProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3aa6176b297261968a63b2f723a65ea14b45b8d3628b200be92df556adc5c2b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129378"
---
# <a name="installeropenproduct-method"></a>OpenProduct 方法

[**安裝程式**](installer-object.md)物件的 **OpenProduct** 方法會使用產品代碼開啟已安裝產品的安裝程式套件，並傳回 [**會話**](session-object.md)物件。

## <a name="syntax"></a>語法


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*productCode* 
</dt> <dd>

必要的字串，其中包含唯一的產品代碼 ([GUID](guid.md)) 或安裝程式所寫入的啟用描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

請注意，單一進程只能開啟一個 [**會話**](session-object.md) 物件。 **OpenProduct** 不能用在自訂動作中，因為使用中的安裝是唯一允許的會話。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




