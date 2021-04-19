---
description: 擴充針對資料列集 Api 定義的屬性。
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba37466c52f2fa9f83e3aa439ace03c1fba34f44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983826"
---
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ MSIDXS \_ ROWSETEXT

擴充針對資料列集 Api 定義的屬性。

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

DBPROPSET \_ MSIDXS \_ ROWSETEXT 屬性集包含下列屬性常數：

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS
</dt> <dd>

屬性識別碼2。 資料列集的查詢狀態。 STAT \_ \* 常數指出執行和可靠性狀態。

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>MSIDXSPROP \_ 命令 \_ 地區設定 \_ 字串
</dt> <dd>

屬性識別碼3。 地區設定字串，表示要用於此資料列集的語言和地區設定。

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP \_ 查詢 \_ 限制
</dt> <dd>

屬性識別碼4。 與此資料列集相關聯的查詢字串。

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP \_ 剖析 \_ 樹狀結構
</dt> <dd>

屬性識別碼5。

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP \_ 最大 \_ 排名 
</dt> <dd>

屬性識別碼6。

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>\_找到 MSIDXSPROP 結果 \_
</dt> <dd>

屬性識別碼7。

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID
</dt> <dd>

屬性識別碼8。

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>MSIDXSPROP \_ 伺服器 \_ 版本 
</dt> <dd>

適用于 Windows 7 的新。 屬性識別碼9。 伺服器版本。

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ 伺服器 \_ WINVER \_ 主要
</dt> <dd>

屬性識別碼10。

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ 伺服器 \_ WINVER \_ 次要
</dt> <dd>

屬性識別碼11。

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP \_ 伺服器 \_ NLSVERSION
</dt> <dd>

屬性識別碼12。

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>\_ \_ 已定義 MSIDXSPROP 伺服器 NLSVER \_ 
</dt> <dd>

屬性識別碼13。

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>使用的 MSIDXSPROP \_ 相同的 \_ SORTORDER \_ 
</dt> <dd>

屬性識別碼14。

</dd> </dl>

## <a name="remarks"></a>備註

若要查詢 MSIDXSPROP \_ server \_ 版本，必須將虛擬查詢發行至伺服器，如下列範例所示。

`SELECT top 1 workid from servername.systemindex`

傳回資料列集之後，請呼叫 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得資料列集的功能，然後針對新的屬性呼叫 [IRowsetInfo：： GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) (MSIDXSPROP \_ SERVER \_ 版本) 。 屬性具有 **VT \_ I4** 的類型，而且可以是下列其中一個值：

\#定義 CI \_ 版本 \_ WDS30 0x102//258

\#定義 CI \_ 版本 \_ WDS40 0x109//265

\#定義 CI \_ 版本 \_ WIN70 0x700//1792

一旦知道值之後，用戶端就可以形成伺服器所支援的查詢，併發出實際的查詢。

DBPROPSET \_ MSIDXS \_ ROWSETEXT 宣告于 ntquery. h 中。

 

 
