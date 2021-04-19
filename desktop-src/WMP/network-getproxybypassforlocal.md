---
title: GetProxyBypassForLocal 方法
description: GetProxyBypassForLocal 方法會抓取值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- getProxyBypassForLocal 方法 Windows Media Player
- getProxyBypassForLocal 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxyBypassForLocal 方法
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992900"
---
# <a name="networkgetproxybypassforlocal-method"></a><span data-ttu-id="084aa-106">GetProxyBypassForLocal 方法</span><span class="sxs-lookup"><span data-stu-id="084aa-106">Network.getProxyBypassForLocal method</span></span>

<span data-ttu-id="084aa-107">**GetProxyBypassForLocal** 方法會抓取值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="084aa-107">The **getProxyBypassForLocal** method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="084aa-108">語法</span><span class="sxs-lookup"><span data-stu-id="084aa-108">Syntax</span></span>


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="084aa-109">參數</span><span class="sxs-lookup"><span data-stu-id="084aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="084aa-110">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="084aa-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084aa-111">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="084aa-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="084aa-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="084aa-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="084aa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="084aa-113">Return value</span></span>

<span data-ttu-id="084aa-114">這個方法會傳回 **布林值** ，指出是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="084aa-114">This method returns a **Boolean** indicating whether the proxy server is bypassed.</span></span> <span data-ttu-id="084aa-115">只有當 **getProxySettings** 傳回兩個 (使用手動設定) 的值時，傳回的值才有意義。</span><span class="sxs-lookup"><span data-stu-id="084aa-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="084aa-116">備註</span><span class="sxs-lookup"><span data-stu-id="084aa-116">Remarks</span></span>

<span data-ttu-id="084aa-117">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="084aa-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="084aa-118">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="084aa-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="084aa-119">範例</span><span class="sxs-lookup"><span data-stu-id="084aa-119">Examples</span></span>

<span data-ttu-id="084aa-120">下列 JScript 範例會使用 *網路*。**getProxyBypassForLocal** 顯示 Windows Media Player 是否設定為略過本機位址的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="084aa-120">The following JScript example uses *Network*.**getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="084aa-121">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="084aa-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a><span data-ttu-id="084aa-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="084aa-122">Requirements</span></span>



| <span data-ttu-id="084aa-123">需求</span><span class="sxs-lookup"><span data-stu-id="084aa-123">Requirement</span></span> | <span data-ttu-id="084aa-124">值</span><span class="sxs-lookup"><span data-stu-id="084aa-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="084aa-125">版本</span><span class="sxs-lookup"><span data-stu-id="084aa-125">Version</span></span><br/> | <span data-ttu-id="084aa-126">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="084aa-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="084aa-127">DLL</span><span class="sxs-lookup"><span data-stu-id="084aa-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="084aa-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="084aa-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="084aa-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="084aa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="084aa-130">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="084aa-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="084aa-131">**GetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="084aa-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





