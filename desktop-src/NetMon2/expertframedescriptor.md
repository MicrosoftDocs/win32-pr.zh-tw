---
description: EXPERTFRAMEDESCRIPTOR 結構包含框架的相關資訊。 當專家成功呼叫 ExpertGetFrame 函式時，網路監視器會將 EXPERTFRAMEDESCRIPTOR 結構傳回給專家。
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: 'EXPERTFRAMEDESCRIPTOR 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468756"
---
# <a name="expertframedescriptor-structure"></a>EXPERTFRAMEDESCRIPTOR 結構

**EXPERTFRAMEDESCRIPTOR** 結構包含框架的相關資訊。 當專家成功呼叫 [**ExpertGetFrame**](expertgetframe.md) 函式時，網路監視器會將 **EXPERTFRAMEDESCRIPTOR** 結構傳回給專家。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a>成員

<dl> <dt>

**FrameNumber**
</dt> <dd>

指定框架的數目。

</dd> <dt>

**hFrame**
</dt> <dd>

框架的控制碼。

</dd> <dt>

**pFrame**
</dt> <dd>

原始框架的指標。

</dd> <dt>

**lpRecognizeDataTable**
</dt> <dd>

資料表，指出每個剖析器識別資料開始的位置。

</dd> <dt>

**lpPropertyTable**
</dt> <dd>

剖析器所識別的框架屬性資料表。

</dd> </dl>

## <a name="remarks"></a>備註

如果專家在 \_ \_ 呼叫 [**EXPERTGETFRAME**](expertgetframe.md)時指定 FLAGS 附加屬性，則每個 [**PROPERTYINST**](propertyinst.md)結構中的 **szPropertyText** 成員都是 **Null**。

如果專家在呼叫 ExpertGetFrame 函式時未指定 FLAGS \_ 附加 \_ 屬性，則在傳回時， [](expertgetframe.md) **lpPropertyTable** 成員會是 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




