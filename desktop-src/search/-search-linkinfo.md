---
description: 儲存連結類型的相關資訊，並由 IItemPreviewerExt 介面使用。
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: LINKINFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97c106a5a819ac1068501c77555f3eae238c935e2262894c6c250dfc6782188f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863941"
---
# <a name="linkinfo-structure"></a>LINKINFO 結構

\[只有 Windows XP 和 Windows Server 2003 支援 **LINKINFO** 和 [**IItemPreviewerExt**](-search-iitempreviewerext.md) ，而且不應該再使用。\]

儲存連結類型的相關資訊，並由 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面使用。

## <a name="syntax"></a>語法


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**type**
</dt> <dd>

類型： **[ **LINKTYPE**](-search-linktype.md)**

</dd> <dd>

[**LINKTYPE**](-search-linktype.md)常數所指出的編目或索引時所指定的連結類型。

</dd> <dt>

**bstrContentType**
</dt> <dd>

類型： **BSTR**

</dd> <dd>

指定內容類型的 **BSTR** 值。

</dd> <dt>

**bstrEncoding**
</dt> <dd>

類型： **BSTR**

</dd> <dd>

在 Web 服務描述語言中指定的 EncodingStyle 屬性 (WSDL) 檔。

</dd> <dt>

**bstrFileExt**
</dt> <dd>

類型： **BSTR**

</dd> <dd>

指定副檔名的 **BSTR** 值。

</dd> <dt>

**varData**
</dt> <dd>

類型： **VARIANT**

</dd> <dd>

指定變數值的 variant。

</dd> <dt>

**dwRelatedParts**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

指定相關元件的 **DWORD** 。

</dd> <dt>

**bstrRelatedCid**
</dt> <dd>

類型： **BSTR**

</dd> <dd>

**BSTR** 值，指定 Cid 屬性（非填補的帶正負號的十進位字串）。

</dd> <dt>

**lCodePage**
</dt> <dd>

類型： **Long**

</dd> <dd>

用來編碼字串的字碼頁。

</dd> </dl>

## <a name="remarks"></a>備註

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **LINKINFO** 結構和下列 api： [**IItemPreviewerExt：： GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md)和 [**IItemPreviewerExt：： GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md)方法和 [**LINKTYPE**](-search-linktype.md)列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>          |



 

 




