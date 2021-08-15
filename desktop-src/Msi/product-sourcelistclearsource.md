---
description: SourceListClearSource 方法會移除網路或 URL 來源。 接受型別、來源型別和 SourcePath （來源路徑）作為要移除的參數。 這個方法會呼叫 MsiSourceListClearSource。
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: SourceListClearSource 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9adeb342aa47162905814979eb29853edd1c5bc660e3771f3beabb8a485c6060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376691"
---
# <a name="productsourcelistclearsource-method"></a>SourceListClearSource 方法

**SourceListClearSource** 方法會移除網路或 URL 來源。 接受 *型* 別、來源型別和 *SourcePath*（來源路徑）作為要移除的參數。 這個方法會呼叫 [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)。

## <a name="syntax"></a>語法


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* 
</dt> <dd>

要移除的來源類型： MSISOURCETYPE \_ NETWORK 或 MSISOURCETYPE \_ URL。

</dd> <dt>

*SourcePath* 
</dt> <dd>

要移除之來源的路徑。

</dd> </dl>

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

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




