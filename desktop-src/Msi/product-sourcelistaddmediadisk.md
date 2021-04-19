---
description: SourceListAddMediaDisk 方法會將磁片新增至已註冊的磁片集。 接受 Diskid、VolumeLabel 和 DiskPrompt 做為參數。 這個方法會在 MsiSourceListAddMediaDisk 上呼叫。
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: SourceListAddMediaDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2f81b21570d708f361e45be7f6f42a93fd0d335
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999325"
---
# <a name="productsourcelistaddmediadisk-method"></a>SourceListAddMediaDisk 方法

**SourceListAddMediaDisk** 方法會將磁片新增至已註冊的磁片集。 接受 *Diskid*、 *VolumeLabel* 和 *DiskPrompt* 做為參數。 這個方法會在 [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)上呼叫。

## <a name="syntax"></a>語法


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*Diskid* 
</dt> <dd>

此參數提供要新增或更新之磁片的識別碼。

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

此參數提供要新增或更新之磁片的標籤。 更新會覆寫登錄中的現有磁片區標籤。 若只要變更磁片提示，請取得現有的已註冊磁片區標籤，並將它與新的磁片提示一起提供。 此參數的空字串會將空字串（長度 (0 位元組）註冊為磁片區標籤) 。

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

此參數會提供要新增或更新之磁片的磁片提示。 更新會覆寫登錄中的現有磁片提示。 若只要變更磁片區標籤，請從登錄中取得現有的磁片提示，並提供新的磁片區標籤。 此參數的空字串會將空字串（長度 (0 位元組）註冊為磁片提示字元) 。

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

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




