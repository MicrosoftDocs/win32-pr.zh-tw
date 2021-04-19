---
title: SetProxyExceptionList 方法
description: SetProxyExceptionList 方法會指定 proxy 例外清單。 |SetProxyExceptionList 方法
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- setProxyExceptionList 方法 Windows Media Player
- setProxyExceptionList 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxyExceptionList 方法
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989251"
---
# <a name="networksetproxyexceptionlist-method"></a><span data-ttu-id="27bd0-107">SetProxyExceptionList 方法</span><span class="sxs-lookup"><span data-stu-id="27bd0-107">Network.setProxyExceptionList method</span></span>

<span data-ttu-id="27bd0-108">**SetProxyExceptionList** 方法會指定 proxy 例外清單。</span><span class="sxs-lookup"><span data-stu-id="27bd0-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="27bd0-109">語法</span><span class="sxs-lookup"><span data-stu-id="27bd0-109">Syntax</span></span>


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a><span data-ttu-id="27bd0-110">參數</span><span class="sxs-lookup"><span data-stu-id="27bd0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27bd0-111">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27bd0-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27bd0-112">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="27bd0-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="27bd0-113">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="27bd0-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="27bd0-114">*清單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27bd0-114">*list* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27bd0-115">**字串** ，指定要略過 proxy 伺服器的主機清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="27bd0-115">**String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27bd0-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="27bd0-116">Return value</span></span>

<span data-ttu-id="27bd0-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="27bd0-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27bd0-118">備註</span><span class="sxs-lookup"><span data-stu-id="27bd0-118">Remarks</span></span>

<span data-ttu-id="27bd0-119">當目標 URL 的主機部分符合清單中的專案時，這是電腦、網域及/或位址的清單，將會略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="27bd0-119">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="27bd0-120">\*字元可以用來做為清單專案的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="27bd0-120">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="27bd0-121">例如， \* .com 會比對 com 網域中的所有主機，而67則 \* 會比對67類別中的所有主機與子網。</span><span class="sxs-lookup"><span data-stu-id="27bd0-121">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="27bd0-122">除非 **getProxySettings** 傳回值 2 () 使用手動設定，否則這個方法沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="27bd0-122">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="27bd0-123">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="27bd0-123">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="27bd0-124">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="27bd0-124">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="27bd0-125">範例</span><span class="sxs-lookup"><span data-stu-id="27bd0-125">Examples</span></span>

<span data-ttu-id="27bd0-126">下列 JScript 範例會使用 *網路*。**setProxyExceptionList** ，指定在使用 MMS 通訊協定時，已略過 proxy 伺服器的主機清單。</span><span class="sxs-lookup"><span data-stu-id="27bd0-126">The following JScript example uses *Network*.**setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="27bd0-127">新的清單會從 ID = ".XLIST" 的 HTML 文字元素中取出。</span><span class="sxs-lookup"><span data-stu-id="27bd0-127">The new list is retrieved from an HTML TEXT element with ID = "XLIST".</span></span> <span data-ttu-id="27bd0-128">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="27bd0-128">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="27bd0-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="27bd0-129">Requirements</span></span>



| <span data-ttu-id="27bd0-130">需求</span><span class="sxs-lookup"><span data-stu-id="27bd0-130">Requirement</span></span> | <span data-ttu-id="27bd0-131">值</span><span class="sxs-lookup"><span data-stu-id="27bd0-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27bd0-132">版本</span><span class="sxs-lookup"><span data-stu-id="27bd0-132">Version</span></span><br/> | <span data-ttu-id="27bd0-133">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="27bd0-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="27bd0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="27bd0-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="27bd0-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27bd0-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27bd0-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27bd0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27bd0-137">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="27bd0-137">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





