---
description: 指定編目或編制索引時的連結類型。
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: LINKTYPE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 16c61f8d92a6f90be0fa4b64ddd9d582987ac0bdf52ca1c596c7db3a7fa4b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463041"
---
# <a name="linktype-enumeration"></a>LINKTYPE 列舉

\[只有 Windows XP 和 Windows Server 2003 才支援 **LINKTYPE** 列舉，因此不應再使用。\]

指定編目或編制索引時的連結類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE \_ URL**
</dt> <dd>

指定是否應編制 Url 連結類型的索引。

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**LINKTYPE \_ 內容**
</dt> <dd>

指定是否應該為連結內容編制索引。

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE \_ 相關**
</dt> <dd>

指定相關的連結。

</dd> </dl>

## <a name="remarks"></a>備註

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能必須使用 **LINKTYPE** 旗標和下列其他 api： [**IItemPreviewerExt：： GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md)和 [**IItemPreviewerExt：： GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md)方法和 [**LINKINFO**](-search-linkinfo.md)結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



 

 




