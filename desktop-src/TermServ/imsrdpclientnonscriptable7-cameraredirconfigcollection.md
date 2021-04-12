---
title: IMsRdpClientNonScriptable7 CameraRedirConfigCollection 屬性
description: 取得 (的攝影機集合，以及可用於重新導向的相關聯設定) 。
ms.tgt_platform: multiple
keywords:
- CameraRedirConfigCollection 屬性遠端桌面服務
- CameraRedirConfigCollection 屬性遠端桌面服務，IMsRdpClientNonScriptable7 介面
- IMsRdpClientNonScriptable7 介面遠端桌面服務，CameraRedirConfigCollection 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104317535"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>IMsRdpClientNonScriptable7：： CameraRedirConfigCollection 屬性

取得 (的攝影機集合，以及可用於重新導向的相關聯設定) 。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a>屬性值

[IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) ，表示 (的相機集合，以及可供重新導向的相關聯設定) 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1803 版 (組建 17134)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 定義為71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>