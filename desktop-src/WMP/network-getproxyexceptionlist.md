---
title: GetProxyExceptionList 方法
description: GetProxyExceptionList 方法會抓取 proxy 例外清單。
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- getProxyExceptionList 方法 Windows Media Player
- getProxyExceptionList 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxyExceptionList 方法
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976214"
---
# <a name="networkgetproxyexceptionlist-method"></a><span data-ttu-id="a339a-106">GetProxyExceptionList 方法</span><span class="sxs-lookup"><span data-stu-id="a339a-106">Network.getProxyExceptionList method</span></span>

<span data-ttu-id="a339a-107">**GetProxyExceptionList** 方法會抓取 proxy 例外清單。</span><span class="sxs-lookup"><span data-stu-id="a339a-107">The **getProxyExceptionList** method retrieves the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a339a-108">語法</span><span class="sxs-lookup"><span data-stu-id="a339a-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyExceptionList(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="a339a-109">參數</span><span class="sxs-lookup"><span data-stu-id="a339a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a339a-110">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a339a-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a339a-111">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="a339a-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="a339a-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a339a-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a339a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a339a-113">Return value</span></span>

<span data-ttu-id="a339a-114">這個方法會傳回 **字串** ，指定要略過 proxy 伺服器的主機清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="a339a-114">This method returns a **String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="a339a-115">只有當 **getProxySettings** 傳回兩個 (使用手動設定) 的值時，傳回的值才有意義。</span><span class="sxs-lookup"><span data-stu-id="a339a-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="a339a-116">備註</span><span class="sxs-lookup"><span data-stu-id="a339a-116">Remarks</span></span>

<span data-ttu-id="a339a-117">當目標 URL 的主機部分符合清單中的專案時，這是電腦、網域及/或位址的清單，將會略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a339a-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="a339a-118">\*字元可以用來做為清單專案的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="a339a-118">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="a339a-119">例如， \* .com 會比對 com 網域中的所有主機（67）。 \* 會比對67類別中的所有主機與子網。</span><span class="sxs-lookup"><span data-stu-id="a339a-119">For example, \*.com would match all hosts in the com domain while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="a339a-120">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="a339a-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="a339a-121">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="a339a-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="a339a-122">範例</span><span class="sxs-lookup"><span data-stu-id="a339a-122">Examples</span></span>

<span data-ttu-id="a339a-123">下列 JScript 範例會使用 *網路*。**getProxyExceptionList** 可顯示 MMS 和 HTTP 通訊協定的已略過 proxy 清單。</span><span class="sxs-lookup"><span data-stu-id="a339a-123">The following JScript example uses *Network*.**getProxyExceptionList** to display the lists of bypassed proxies for the MMS and HTTP protocols.</span></span> <span data-ttu-id="a339a-124">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="a339a-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

```



## <a name="requirements"></a><span data-ttu-id="a339a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a339a-125">Requirements</span></span>



| <span data-ttu-id="a339a-126">需求</span><span class="sxs-lookup"><span data-stu-id="a339a-126">Requirement</span></span> | <span data-ttu-id="a339a-127">值</span><span class="sxs-lookup"><span data-stu-id="a339a-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a339a-128">版本</span><span class="sxs-lookup"><span data-stu-id="a339a-128">Version</span></span><br/> | <span data-ttu-id="a339a-129">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a339a-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a339a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a339a-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="a339a-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a339a-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a339a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a339a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a339a-133">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="a339a-133">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="a339a-134">**GetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="a339a-134">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





