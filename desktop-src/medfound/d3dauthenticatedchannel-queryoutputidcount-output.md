---
description: 包含對 D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT 查詢的回應。
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: 'D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: c97f55d05aff3feb1857456ec04c4fa48872487decc5812912081b894896dce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777548"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ 輸出結構

包含對 [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) 查詢的回應。

若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**輸出**
</dt> <dd>

包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。

</dd> <dt>

**DeviceHandle**
</dt> <dd>

裝置的控制碼。

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

密碼編譯會話的控制碼。

</dd> <dt>

**NumOutputIDs**
</dt> <dd>

與指定裝置和密碼編譯會話相關聯的輸出識別碼數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片結構](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




