---
description: Product 物件的 SourceListClearMediaDisk 方法會從產品的已註冊磁片集中移除指定的磁片。 接受 Diskid 做為參數。 這個方法會呼叫 MsiSourceListClearMediaDisk。
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: SourceListClearMediaDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a607591f45208854118b0f97849cd7072e484bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989517"
---
# <a name="productsourcelistclearmediadisk-method"></a>SourceListClearMediaDisk 方法

[**Product**](product-object.md)物件的 **SourceListClearMediaDisk** 方法會從產品的已註冊磁片集中移除指定的磁片。 接受 *Diskid* 做為參數。 這個方法會呼叫 [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)。

## <a name="syntax"></a>語法


```JScript
Product.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*Diskid* 
</dt> <dd>

此參數提供要移除之磁片的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**產品**](product-object.md)
</dt> <dt>

[**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




