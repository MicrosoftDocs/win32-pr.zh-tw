---
description: 包含對 D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES 查詢的回應。
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: 'D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970743"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_ 輸出結構

包含對 [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) 查詢的回應。

若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**輸出**
</dt> <dd>

包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。

</dd> <dt>

**BusType**
</dt> <dd>

來自 [**D3DBUSTYPE**](d3dbustype.md)列舉之旗標的位 **or** 。

</dd> <dt>

**bAccessibleInContiguousBlocks**
</dt> <dd>

若 **為 TRUE**，則 CPU 或匯流排可以存取影片記憶體的連續區塊。

</dd> <dt>

**bAccessibleInNonContiguousBlocks**
</dt> <dd>

若 **為 TRUE**，則 CPU 或匯流排可以存取非連續的影片記憶體區塊。

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

 

 




