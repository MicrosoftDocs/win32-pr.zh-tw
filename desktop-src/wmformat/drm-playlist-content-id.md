---
title: 'DRM_PLAYLIST_CONTENT_ID 結構 (Drmexternals .h) '
description: DRM \_ 播放清單 \_ 內容 \_ 識別碼結構包含在播放清單燒錄時複製到 CD 的內容相關資訊。
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- DRM_PLAYLIST_CONTENT_ID 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967352"
---
# <a name="drm_playlist_content_id-structure"></a>DRM \_ 播放清單 \_ 內容 \_ 識別碼結構

**DRM \_ 播放清單 \_ 內容 \_ 識別碼** 結構包含在播放清單燒錄時複製到 CD 的內容相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**lpcwszV2Header**
</dt> <dd>

DRM 標頭。 如果內容受到 Windows Media DRM 第2版或更新版本的保護，請使用這個成員。

</dd> <dt>

**lpcszV1KID**
</dt> <dd>

金鑰識別碼。 如果內容受到 Windows Media DRM 第1版的保護，請使用這個成員。

</dd> <dt>

**pbOtherData**
</dt> <dd>

包含補充資料的緩衝區。

</dd> <dt>

**cbOtherData**
</dt> <dd>

**PbOtherData** 緩衝區的大小（以位元組為單位）。

</dd> <dt>

**dwUniqueIDForSession**
</dt> <dd>

要在目前會話中使用之內容的唯一識別碼。

</dd> <dt>

**dwValidFields**
</dt> <dd>

**DWORD** ，表示此結構的有效欄位。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                      |
| 版本<br/>                  | Windows Media Format 11 SDK<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>Drmexternals。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





