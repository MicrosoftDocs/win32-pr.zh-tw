---
description: 包含對 D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION 查詢的回應。
ms.assetid: df9d9b41-8188-4597-9e83-d14065eb7fc7
title: 'D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fb4e6ccad999f183e71f0f57d64544a70cef5534
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971983"
---
# <a name="d3dauthenticatedchannel_querycryptosession_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_ 輸出結構

包含對 [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) 查詢的回應。

若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DXVA2DecodeHandle;
  HANDLE                               CryptoSessionHandle;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**輸出**
</dt> <dd>

包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。

</dd> <dt>

**DXVA2DecodeHandle**
</dt> <dd>

DirectX Video 加速 2 (DXVA-2) 解碼器裝置的控制碼。

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

與解碼器裝置相關聯的密碼編譯會話控制碼。

</dd> <dt>

**DeviceHandle**
</dt> <dd>

與解碼器裝置相關聯之 Direct3D 裝置的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片結構](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




