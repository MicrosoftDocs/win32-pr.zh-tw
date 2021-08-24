---
description: SourceListForceResolution 方法會清除 LastUsedSource 屬性。
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: SourceListForceResolution 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3215f5b43200cb8ca43fba36dc71e1a582aa24b92904e2c48268245921a2ccf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754008"
---
# <a name="productsourcelistforceresolution-method"></a>SourceListForceResolution 方法

**SourceListForceResolution** 方法會清除 LastUsedSource 屬性。 這會強制安裝程式在下次需要來源時，在來源清單中搜尋有效的產品來源，例如，當安裝程式執行安裝或重新安裝時，或是當元件設定為從來源執行時需要路徑。

這個方法會呼叫 [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)。

## <a name="syntax"></a>語法


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003、Windows XP 和 Windows 2000 上的安裝程式3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**產品**](product-object.md)
</dt> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




