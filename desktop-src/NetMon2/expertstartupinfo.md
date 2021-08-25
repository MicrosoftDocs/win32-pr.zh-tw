---
description: 包含在開始時描述專家的資料。
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: 'EXPERTSTARTUPINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f49fcf3c87795dbd7c9e65745e1b5560331c96c471d8ff7b2c8a24560b143cb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911048"
---
# <a name="expertstartupinfo-structure"></a>EXPERTSTARTUPINFO 結構

**EXPERTSTARTUPINFO** 結構包含的資料會在開始時描述專家。

## <a name="syntax"></a>語法


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**旗標**
</dt> <dd>

描述專家的旗標。

</dd> <dt>

**hCapture**
</dt> <dd>

捕捉的控制碼。

</dd> <dt>

**szCaptureFile**
</dt> <dd>

Capture 檔案的名稱。

</dd> <dt>

**dwFrameNumber**
</dt> <dd>

畫面格編號。

</dd> <dt>

**hProtocol**
</dt> <dd>

通訊協定的控制碼。

</dd> <dt>

**lpPropertyInst**
</dt> <dd>

[**PROPERTYINST**](propertyinst.md)結構的指標。

</dd> <dt>

**sBitfield**
</dt> <dd> <dl> <dt>

**BitNumber**
</dt> <dd>

只有在 [**PROPERTYINST**](propertyinst.md)結構的 **DataQualifier** 成員設定為 [ \_ QUAL] 旗標時，才會使用 \_ 。

</dd> <dt>

**邦**
</dt> <dd>

只有在 [**PROPERTYINST**](propertyinst.md)結構的 **DataQualifier** 成員設定為 [ \_ QUAL] 旗標時，才會使用 \_ 。

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




