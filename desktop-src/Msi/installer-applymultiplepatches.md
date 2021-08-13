---
description: ApplyMultiplePatches 方法會將一或多個修補程式套用至有資格接收修補程式的產品。 方法會設定 PATCH 屬性。
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: ApplyMultiplePatches 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a2b1c469ca623b0c09ea2899de1867cc10c8d8cda9363994973d08ecc20ed7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633205"
---
# <a name="installerapplymultiplepatches-method"></a>ApplyMultiplePatches 方法

**ApplyMultiplePatches** 方法會將一或多個修補程式套用至有資格接收修補程式的產品。 方法會設定 [**PATCH**](patch.md) 屬性。

## <a name="syntax"></a>語法


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*PatchPackagesList* 
</dt> <dd>

字串，包含要修補檔案之路徑的分號分隔清單。 例如： "" c： \\ sus 下載快取 \\ \\ \\ Office \\ sp1 .msp;c： \\ sus \\ 下載快取 \\ \\ Office \\ QFE1 .msp; c： su 下載快取 \\ \\ \\ \\ Office \\ QFEn .msp ""

</dd> <dt>

*產品* 
</dt> <dd>

此參數提供所修補產品的 [**ProductCode**](productcode.md) 。 這是選擇性參數。 當此參數為 null 時，會將修補程式套用至有資格接收這些修補程式的所有產品。

</dd> <dt>

*szPropertiesList* 
</dt> <dd>

指定命令列屬性設定的以 null 終止的字串。 這是選擇性參數。 請參閱 [關於屬性](about-properties.md) ，並 [在命令列上設定公用屬性值](setting-public-property-values-on-the-command-line.md)。 這些屬性會由所有目標產品共用。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式3.0 或更新版本。<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[關於屬性](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**補丁**](patch.md)
</dt> <dt>

[在命令列上設定公用屬性值](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




