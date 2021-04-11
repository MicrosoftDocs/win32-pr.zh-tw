---
description: 包含檔案的屬性資料。
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: ATTRINFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847012"
---
# <a name="attrinfo-structure"></a>ATTRINFO 結構

包含檔案的屬性資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**tAttrID**
</dt> <dd>

屬性類型。 請參閱 [標記類型](tag-types.md)。

</dd> <dt>

**dwFlags**
</dt> <dd>

這個屬性的旗標。



| 值                                                                                                                                                                                                                                           | 意義                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**屬性 \_可用**</dt>的 <dt>0x00000001</dt> </dl> | 屬性可供使用。<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**屬性 \_失敗**</dt>的 <dt>0x00000002</dt> </dl>          | 因為無法使用屬性，所以呼叫失敗。<br/> |



 

</dd> <dt>

**ullAttr**
</dt> <dd>

如果標記類型為 **\_ \_ qword) 標記** 類型，則為 **qword** 值 (。

</dd> <dt>

**dwAttr**
</dt> <dd>

**Dword** 值 (如果標記類型為 **標記 \_ 類型 \_ DWORD**) 。

</dd> <dt>

**lpAttr**
</dt> <dd>

如果標記類型為 **標記 \_ 類型 \_ STRINGREF**) ，則為字串 (的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




