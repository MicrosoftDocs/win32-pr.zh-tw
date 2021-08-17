---
title: IMsRdpClientAdvancedSettings8 BandwidthDetection 屬性
description: 指定是否自動偵測頻寬變更。
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- BandwidthDetection 屬性遠端桌面服務
- BandwidthDetection 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，BandwidthDetection 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ab6fbe8291c0318e378add8041d0e2d2d0f30b6ee1e298c3a43a6a0ccd430c31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138781"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a>IMsRdpClientAdvancedSettings8：： BandwidthDetection 屬性

指定是否自動偵測頻寬變更。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a>屬性值

**變異 \_** 如果自動偵測到頻寬變更，則為 TRUE，否則為 **VARIANT \_ FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





