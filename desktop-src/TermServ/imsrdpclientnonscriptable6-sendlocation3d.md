---
title: IMsRdpClientNonScriptable6 SendLocation3D 方法
description: 將緯度、經度和海拔值傳送至伺服器，讓用戶端的地理位置可以反映在遠端會話中。
ms.tgt_platform: multiple
keywords:
- SendLocation3D 方法遠端桌面服務
- SendLocation3D 方法遠端桌面服務，IMsRdpClientNonScriptable6 介面
- IMsRdpClientNonScriptable6 介面遠端桌面服務，SendLocation3D 方法
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104467392"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a>IMsRdpClientNonScriptable6：： SendLocation3D 方法

將緯度、經度和海拔值傳送至伺服器，讓用戶端的地理位置可以反映在遠端會話中。

## <a name="syntax"></a>語法

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a>參數

*緯度* \[在\]

地理位置的緯度。 緯度值的有效範圍是從-90.0 到90.0 度。

*經度* \[在\]

地理位置的經度。 緯度值的有效範圍是從-180.0 到180.0 度。

*高度* \[在\]

地理位置的高度（以量為單位）。

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1709 版 (組建 16299)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable6 定義為 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
