---
description: 包含 IDirect3DAuthenticatedChannel9：： Query 方法的回應。
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: 'D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2defeaf134db9a2464854554db721586f592fc62110d172e0ac804e010804966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600828"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出結構

包含 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) 方法的回應。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**omac**
</dt> <dd>

[**D3D \_ OMAC**](d3d-omac.md)結構，其中包含資料的訊息驗證碼 (MAC) 。 驅動程式會使用 AES 型單鍵 CBC MAC (OMAC) 為此結構成員後面出現的資料區塊計算此值。

</dd> <dt>

**QueryType**
</dt> <dd>

指定查詢的 GUID。 如需值的清單，請參閱 [內容保護查詢](content-protection-queries.md)。

</dd> <dt>

**處理**
</dt> <dd>

已驗證通道的控制碼。

</dd> <dt>

**UINT**
</dt> <dd>

查詢序號。

</dd> <dt>

**ReturnCode**
</dt> <dd>

查詢的結果碼。

</dd> </dl>

## <a name="remarks"></a>備註

針對 **QueryType**、 **hChannel** 和 **SequenceNumber** 成員，驅動程式會使用與應用程式在 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md) 結構中所提供的相同值。 應用程式應該驗證這些值是否相符。

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

 

 




