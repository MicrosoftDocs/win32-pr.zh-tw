---
title: IMsRdpClientAdvancedSettings7 VideoPlaybackMode 屬性
description: 指定或抓取表示影片播放模式的值。
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- VideoPlaybackMode 屬性遠端桌面服務
- VideoPlaybackMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，VideoPlaybackMode 屬性
- VideoPlaybackMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，VideoPlaybackMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385286"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a>IMsRdpClientAdvancedSettings7：： VideoPlaybackMode 屬性

指定或抓取表示影片播放模式的值。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a>屬性值

指定影片播放模式的值。

可能的值包括：

<dt>

1
</dt> <dd>

預設的影片播放模式。 當影片播放模式設定為此值時，影片重新導向是由 [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) 屬性所控制。 當 [ **AudioRedirectionMode** ] 屬性設定為 [ **音訊 \_ 模式重新 \_ 導向]** 時，會在用戶端上將影片解碼和轉譯。

</dd> <dt>

0
</dt> <dd>

即使 [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) 設為 **音訊 \_ 模式重新 \_ 導向**，也會停用影片播放重新導向。 在此模式中，影片會在 RD 工作階段主機伺服器上進行解碼和轉譯。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                                |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





