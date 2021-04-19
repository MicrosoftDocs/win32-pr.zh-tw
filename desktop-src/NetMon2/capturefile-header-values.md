---
description: 定義網路監視器標頭檔結構。
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: 'CAPTUREFILE_HEADER_VALUES 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974664"
---
# <a name="capturefile_header_values-structure"></a>CAPTUREFILE \_ 標頭 \_ 值結構

**CAPTUREFILE \_ 標頭 \_ 值** 結構會定義網路監視器標頭檔結構。

## <a name="syntax"></a>語法


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a>成員

<dl> <dt>

**簽名**
</dt> <dd>

唯一識別碼： ' GMBU。

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

二進位、編碼的十進位 (次要) 。 此成員的值應該是零 (0) 。

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

二進位編碼的 decimal (主要) 。 此值應該是2。

</dd> <dt>

**MacType**
</dt> <dd>

拓撲類型。

</dd> <dt>

**時間 戳**
</dt> <dd>

拍攝時間。

</dd> <dt>

**FrameTableOffset**
</dt> <dd>

框架索引表。

</dd> <dt>

**FrameTableLength**
</dt> <dd>

框架索引資料表大小。

</dd> <dt>

**UserDataOffset**
</dt> <dd>

使用者資料位移。

</dd> <dt>

**UserDataLength**
</dt> <dd>

使用者資料長度。

</dd> <dt>

**CommentDataOffset**
</dt> <dd>

批註資料位移。

</dd> <dt>

**CommentDataLength**
</dt> <dd>

批註資料的長度。

</dd> <dt>

**StatisticsOffset**
</dt> <dd>

**統計資料** 結構的位移。

</dd> <dt>

**StatisticsLength**
</dt> <dd>

**統計資料** 結構的長度。

</dd> <dt>

**NetworkInfoOffset**
</dt> <dd>

**NETWORKINFO** 結構的位移。

</dd> <dt>

**NetworkInfoLength**
</dt> <dd>

**NETWORKINFO** 結構的長度。

</dd> <dt>

**ConversationStatsOffset**
</dt> <dd>

未使用這個成員。

</dd> <dt>

**ConversationStatsLength**
</dt> <dd>

未使用這個成員。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




