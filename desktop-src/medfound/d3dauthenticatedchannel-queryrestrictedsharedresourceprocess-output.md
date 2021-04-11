---
description: 包含對 D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS 查詢的回應。
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: 'D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bd93e1cadb7da500a82218924044af79fbb1f493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111809"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ 輸出結構

包含對 [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) 查詢的回應。

若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**輸出**
</dt> <dd>

包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。

</dd> <dt>

**ProcessIndex**
</dt> <dd>

進程清單中進程的索引。

</dd> <dt>

**ProcessIdentifer**
</dt> <dd>

指定進程類型的 [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) 值。

</dd> <dt>

**ProcessHandle**
</dt> <dd>

進程控制碼。 如果 **ProcessIdentifier** 成員等於 **PROCESSIDTYPE \_ 控制碼**， **ProcessHandle** 成員就會包含有效的進程控制碼。 否則，會忽略這個成員。

</dd> </dl>

## <a name="remarks"></a>備註

桌面視窗管理員 (DWM) 進程是藉由設定等於 **PROCESSIDTYPE \_ Dwm** 的 **ProcessIdentifier** 來識別。 其他進程的識別方式是在 **ProcessHandle** 中設定進程控制碼，並設定 **ProcessIdentifier** 等於 **PROCESSIDTYPE \_ 控制碼**。

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

 

 




