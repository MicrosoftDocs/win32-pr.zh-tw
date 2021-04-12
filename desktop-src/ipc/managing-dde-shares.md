---
description: Network DDE 提供可讓您刪除共用、取得或設定共用資訊，或列舉共用的函式。
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: 管理 DDE 共用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321356"
---
# <a name="managing-dde-shares"></a><span data-ttu-id="1f486-103">管理 DDE 共用</span><span class="sxs-lookup"><span data-stu-id="1f486-103">Managing DDE Shares</span></span>

<span data-ttu-id="1f486-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="1f486-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="1f486-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="1f486-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="1f486-106">Network DDE 提供可讓您刪除共用、取得或設定共用資訊，或列舉共用的函式。</span><span class="sxs-lookup"><span data-stu-id="1f486-106">Network DDE provides functions that allow you to delete a share, get or set share information, or enumerate shares.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f486-107">Task</span><span class="sxs-lookup"><span data-stu-id="1f486-107">Task</span></span></th>
<th><span data-ttu-id="1f486-108">程序</span><span class="sxs-lookup"><span data-stu-id="1f486-108">Procedure</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f486-109">刪除 DDE 共用</span><span class="sxs-lookup"><span data-stu-id="1f486-109">Delete a DDE share</span></span></td>
<td><span data-ttu-id="1f486-110">使用 <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="1f486-110">Use the <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f486-111">取得 DDE 共用資訊</span><span class="sxs-lookup"><span data-stu-id="1f486-111">Get DDE share information</span></span></td>
<td><span data-ttu-id="1f486-112">使用 <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="1f486-112">Use the <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f486-113">設定 DDE 共用資訊</span><span class="sxs-lookup"><span data-stu-id="1f486-113">Set DDE share information</span></span></td>
<td><span data-ttu-id="1f486-114">使用 <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="1f486-114">Use the <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f486-115">列舉 DDE 共用</span><span class="sxs-lookup"><span data-stu-id="1f486-115">Enumerate DDE shares</span></span></td>
<td><span data-ttu-id="1f486-116">使用 <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="1f486-116">Use the <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> function.</span></span> <span data-ttu-id="1f486-117">您也可以使用 <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> 函數來列舉受信任的 DDE 共用。</span><span class="sxs-lookup"><span data-stu-id="1f486-117">You can also enumerate the trusted DDE shares by using the <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f486-118">列舉已連線的使用者</span><span class="sxs-lookup"><span data-stu-id="1f486-118">Enumerate connected users</span></span></td>
<td><span data-ttu-id="1f486-119">使用 <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="1f486-119">Use the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f486-120">變更 DDE 共用名稱</span><span class="sxs-lookup"><span data-stu-id="1f486-120">Change the DDE share name</span></span></td>
<td><span data-ttu-id="1f486-121">刪除舊的共用並建立新的共用。</span><span class="sxs-lookup"><span data-stu-id="1f486-121">Delete the old share and create a new share.</span></span>
<ol>
<li><span data-ttu-id="1f486-122">使用 <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>取出共用資訊。</span><span class="sxs-lookup"><span data-stu-id="1f486-122">Retrieve the share information using <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="1f486-123">使用 <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>移除共用。</span><span class="sxs-lookup"><span data-stu-id="1f486-123">Remove the share using <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span></span></li>
<li><span data-ttu-id="1f486-124">變更<a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>所傳回之<a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a>結構的<strong>lpszShareName</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="1f486-124">Change the <strong>lpszShareName</strong> member of the <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure returned by <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="1f486-125">將修改過的 <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> 結構傳遞至 <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1f486-125">Pass the modified <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure to <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

