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
# <a name="dbpropset_msidxs_rowsetext"></a><span data-ttu-id="e2413-103">DBPROPSET \_ MSIDXS \_ ROWSETEXT</span><span class="sxs-lookup"><span data-stu-id="e2413-103">DBPROPSET\_MSIDXS\_ROWSETEXT</span></span>

<span data-ttu-id="e2413-104">擴充針對資料列集 Api 定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2413-104">Extends properties defined for the Rowset APIs.</span></span>

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

<span data-ttu-id="e2413-105">DBPROPSET \_ MSIDXS \_ ROWSETEXT 屬性集包含下列屬性常數：</span><span class="sxs-lookup"><span data-stu-id="e2413-105">The DBPROPSET\_MSIDXS\_ROWSETEXT property set contains the following property constants:</span></span>

<dl> <dt>

<span data-ttu-id="e2413-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS</span><span class="sxs-lookup"><span data-stu-id="e2413-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP\_ROWSETQUERYSTATUS</span></span>
</dt> <dd>

<span data-ttu-id="e2413-107">屬性識別碼2。</span><span class="sxs-lookup"><span data-stu-id="e2413-107">Property ID 2.</span></span> <span data-ttu-id="e2413-108">資料列集的查詢狀態。</span><span class="sxs-lookup"><span data-stu-id="e2413-108">Query status for the rowset.</span></span> <span data-ttu-id="e2413-109">STAT \_ \* 常數指出執行和可靠性狀態。</span><span class="sxs-lookup"><span data-stu-id="e2413-109">The STAT\_\* constants indicate the execution and reliability status.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>MSIDXSPROP \_ 命令 \_ 地區設定 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="e2413-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>MSIDXSPROP\_COMMAND\_LOCALE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="e2413-111">屬性識別碼3。</span><span class="sxs-lookup"><span data-stu-id="e2413-111">Property ID 3.</span></span> <span data-ttu-id="e2413-112">地區設定字串，表示要用於此資料列集的語言和地區設定。</span><span class="sxs-lookup"><span data-stu-id="e2413-112">Locale string that represents the language and locale setting to use for this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP \_ 查詢 \_ 限制</span><span class="sxs-lookup"><span data-stu-id="e2413-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP\_QUERY\_RESTRICTION</span></span>
</dt> <dd>

<span data-ttu-id="e2413-114">屬性識別碼4。</span><span class="sxs-lookup"><span data-stu-id="e2413-114">Property ID 4.</span></span> <span data-ttu-id="e2413-115">與此資料列集相關聯的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="e2413-115">The query string associated with this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP \_ 剖析 \_ 樹狀結構</span><span class="sxs-lookup"><span data-stu-id="e2413-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP\_PARSE\_TREE</span></span>
</dt> <dd>

<span data-ttu-id="e2413-117">屬性識別碼5。</span><span class="sxs-lookup"><span data-stu-id="e2413-117">Property ID 5.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP \_ 最大 \_ 排名</span><span class="sxs-lookup"><span data-stu-id="e2413-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP\_MAX\_RANK</span></span> 
</dt> <dd>

<span data-ttu-id="e2413-119">屬性識別碼6。</span><span class="sxs-lookup"><span data-stu-id="e2413-119">Property ID 6.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>\_找到 MSIDXSPROP 結果 \_</span><span class="sxs-lookup"><span data-stu-id="e2413-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>MSIDXSPROP\_RESULTS\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="e2413-121">屬性識別碼7。</span><span class="sxs-lookup"><span data-stu-id="e2413-121">Property ID 7.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID</span><span class="sxs-lookup"><span data-stu-id="e2413-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP\_WHEREID</span></span>
</dt> <dd>

<span data-ttu-id="e2413-123">屬性識別碼8。</span><span class="sxs-lookup"><span data-stu-id="e2413-123">Property ID 8.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>MSIDXSPROP \_ 伺服器 \_ 版本</span><span class="sxs-lookup"><span data-stu-id="e2413-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>MSIDXSPROP\_SERVER\_VERSION</span></span> 
</dt> <dd>

<span data-ttu-id="e2413-125">適用于 Windows 7 的新。</span><span class="sxs-lookup"><span data-stu-id="e2413-125">New for Windows 7.</span></span> <span data-ttu-id="e2413-126">屬性識別碼9。</span><span class="sxs-lookup"><span data-stu-id="e2413-126">Property ID 9.</span></span> <span data-ttu-id="e2413-127">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="e2413-127">The server version.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ 伺服器 \_ WINVER \_ 主要</span><span class="sxs-lookup"><span data-stu-id="e2413-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP\_SERVER\_WINVER\_MAJOR</span></span>
</dt> <dd>

<span data-ttu-id="e2413-129">屬性識別碼10。</span><span class="sxs-lookup"><span data-stu-id="e2413-129">Property ID 10.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ 伺服器 \_ WINVER \_ 次要</span><span class="sxs-lookup"><span data-stu-id="e2413-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP\_SERVER\_WINVER\_MINOR</span></span>
</dt> <dd>

<span data-ttu-id="e2413-131">屬性識別碼11。</span><span class="sxs-lookup"><span data-stu-id="e2413-131">Property ID 11.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP \_ 伺服器 \_ NLSVERSION</span><span class="sxs-lookup"><span data-stu-id="e2413-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP\_SERVER\_NLSVERSION</span></span>
</dt> <dd>

<span data-ttu-id="e2413-133">屬性識別碼12。</span><span class="sxs-lookup"><span data-stu-id="e2413-133">Property ID 12.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>\_ \_ 已定義 MSIDXSPROP 伺服器 NLSVER \_</span><span class="sxs-lookup"><span data-stu-id="e2413-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP\_SERVER\_NLSVER\_DEFINED</span></span> 
</dt> <dd>

<span data-ttu-id="e2413-135">屬性識別碼13。</span><span class="sxs-lookup"><span data-stu-id="e2413-135">Property ID 13.</span></span>

</dd> <dt>

<span data-ttu-id="e2413-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>使用的 MSIDXSPROP \_ 相同的 \_ SORTORDER \_</span><span class="sxs-lookup"><span data-stu-id="e2413-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP\_SAME\_SORTORDER\_USED</span></span> 
</dt> <dd>

<span data-ttu-id="e2413-137">屬性識別碼14。</span><span class="sxs-lookup"><span data-stu-id="e2413-137">Property ID 14.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2413-138">備註</span><span class="sxs-lookup"><span data-stu-id="e2413-138">Remarks</span></span>

<span data-ttu-id="e2413-139">若要查詢 MSIDXSPROP \_ server \_ 版本，必須將虛擬查詢發行至伺服器，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="e2413-139">To query MSIDXSPROP\_SERVER\_VERSION, it is necessary to issue the dummy query to server, such as the following example.</span></span>

`SELECT top 1 workid from servername.systemindex`

<span data-ttu-id="e2413-140">傳回資料列集之後，請呼叫 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得資料列集的功能，然後針對新的屬性呼叫 [IRowsetInfo：： GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) (MSIDXSPROP \_ SERVER \_ 版本) 。</span><span class="sxs-lookup"><span data-stu-id="e2413-140">After the rowset has been returned, call [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the capabilities of the rowset and then call [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) for the new property (MSIDXSPROP\_SERVER\_VERSION).</span></span> <span data-ttu-id="e2413-141">屬性具有 **VT \_ I4** 的類型，而且可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="e2413-141">The property has a type of **VT\_I4** and can be one of the following values:</span></span>

<span data-ttu-id="e2413-142">\#定義 CI \_ 版本 \_ WDS30 0x102//258</span><span class="sxs-lookup"><span data-stu-id="e2413-142">\#define CI\_VERSION\_WDS30 0x102 // 258</span></span>

<span data-ttu-id="e2413-143">\#定義 CI \_ 版本 \_ WDS40 0x109//265</span><span class="sxs-lookup"><span data-stu-id="e2413-143">\#define CI\_VERSION\_WDS40 0x109 // 265</span></span>

<span data-ttu-id="e2413-144">\#定義 CI \_ 版本 \_ WIN70 0x700//1792</span><span class="sxs-lookup"><span data-stu-id="e2413-144">\#define CI\_VERSION\_WIN70 0x700 // 1792</span></span>

<span data-ttu-id="e2413-145">一旦知道值之後，用戶端就可以形成伺服器所支援的查詢，併發出實際的查詢。</span><span class="sxs-lookup"><span data-stu-id="e2413-145">Once the value is known, the client can form a query which is supported by the server and issue a real query.</span></span>

<span data-ttu-id="e2413-146">DBPROPSET \_ MSIDXS \_ ROWSETEXT 宣告于 ntquery. h 中。</span><span class="sxs-lookup"><span data-stu-id="e2413-146">DBPROPSET\_MSIDXS\_ROWSETEXT is declared in ntquery.h.</span></span>

 

 
