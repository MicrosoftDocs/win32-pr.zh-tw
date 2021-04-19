---
description: 擴充 ITablet 介面。
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: ITablet2 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980619"
---
# <a name="itablet2-interface"></a>ITablet2 介面

擴充 [**ITablet 介面**](itablet.md)。

## <a name="members"></a>成員

**ITablet2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITablet2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITablet2** 介面具有這些方法。



| 方法                                          | 描述                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**GetDeviceKind**](itablet2-getdevicekind.md) | 傳回 tablet 物件所代表的硬體裝置類型，例如滑鼠、畫筆或觸控。<br/> |



 

## <a name="remarks"></a>備註

此介面是在 Windows Vista 中引進的。

開發人員不應使用此介面。

下列程式碼說明如何定義 **ITablet2** 介面。

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

