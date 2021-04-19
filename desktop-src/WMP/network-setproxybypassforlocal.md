---
title: SetProxyBypassForLocal 方法
description: SetProxyBypassForLocal 方法會指定一個值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- setProxyBypassForLocal 方法 Windows Media Player
- setProxyBypassForLocal 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxyBypassForLocal 方法
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984088"
---
# <a name="networksetproxybypassforlocal-method"></a><span data-ttu-id="64d17-106">SetProxyBypassForLocal 方法</span><span class="sxs-lookup"><span data-stu-id="64d17-106">Network.setProxyBypassForLocal method</span></span>

<span data-ttu-id="64d17-107">**SetProxyBypassForLocal** 方法會指定一個值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="64d17-107">The **setProxyBypassForLocal** method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d17-108">語法</span><span class="sxs-lookup"><span data-stu-id="64d17-108">Syntax</span></span>


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a><span data-ttu-id="64d17-109">參數</span><span class="sxs-lookup"><span data-stu-id="64d17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d17-110">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64d17-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d17-111">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="64d17-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="64d17-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="64d17-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="64d17-113">*略過* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64d17-113">*bypass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d17-114">**布林值** ，指定是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="64d17-114">**Boolean** specifying whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d17-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="64d17-115">Return value</span></span>

<span data-ttu-id="64d17-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="64d17-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d17-117">備註</span><span class="sxs-lookup"><span data-stu-id="64d17-117">Remarks</span></span>

<span data-ttu-id="64d17-118">除非 **getProxySettings** 傳回值 2 () 使用手動設定，否則這個方法沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="64d17-118">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="64d17-119">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="64d17-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="64d17-120">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="64d17-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="64d17-121">範例</span><span class="sxs-lookup"><span data-stu-id="64d17-121">Examples</span></span>

<span data-ttu-id="64d17-122">下列 JScript 範例會使用 *網路*。如果源伺服器是在區域網路上，則使用 **setProxyBypassForLocal** 來指定是否略過 Windows Media Player 的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="64d17-122">The following JScript example uses *Network*.**setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="64d17-123">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="64d17-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="64d17-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="64d17-124">Requirements</span></span>



| <span data-ttu-id="64d17-125">需求</span><span class="sxs-lookup"><span data-stu-id="64d17-125">Requirement</span></span> | <span data-ttu-id="64d17-126">值</span><span class="sxs-lookup"><span data-stu-id="64d17-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64d17-127">版本</span><span class="sxs-lookup"><span data-stu-id="64d17-127">Version</span></span><br/> | <span data-ttu-id="64d17-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="64d17-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="64d17-129">DLL</span><span class="sxs-lookup"><span data-stu-id="64d17-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="64d17-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64d17-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d17-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64d17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d17-132">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="64d17-132">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





