---
title: IMsRdpClientNonScriptable7 DisableDpiCursorScalingForProcess 方法
description: 停用從伺服器收到的滑鼠游標區域調整，以確保正確轉譯資料指標圖形，而不進行修改。
ms.tgt_platform: multiple
keywords:
- DisableDpiCursorScalingForProcess 方法遠端桌面服務
- DisableDpiCursorScalingForProcess 方法遠端桌面服務，IMsRdpClientNonScriptable7 介面
- IMsRdpClientNonScriptable7 介面遠端桌面服務，DisableDpiCursorScalingForProcess 方法
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.DisableDpiCursorScalingForProcess
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: a0de989fb0b1c3c644c73f214d368f2cab2ba5d5
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104317539"
---
# <a name="imsrdpclientnonscriptable7disabledpicursorscalingforprocess-method"></a>IMsRdpClientNonScriptable7：:D isableDpiCursorScalingForProcess 方法

停用從伺服器收到的滑鼠游標區域調整，以確保正確轉譯資料指標圖形，而不進行修改。

## <a name="syntax"></a>語法

```C++
HRESULT DisableDpiCursorScalingForProcess();
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

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
