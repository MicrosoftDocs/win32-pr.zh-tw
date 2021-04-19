---
title: GetProxyName 方法
description: GetProxyName 方法會抓取正在使用之 proxy 伺服器的名稱。
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- getProxyName 方法 Windows Media Player
- getProxyName 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxyName 方法
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97e51508e9df9aeac85dbc01116e80e710dcb45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001892"
---
# <a name="networkgetproxyname-method"></a><span data-ttu-id="f756d-106">GetProxyName 方法</span><span class="sxs-lookup"><span data-stu-id="f756d-106">Network.getProxyName method</span></span>

<span data-ttu-id="f756d-107">**GetProxyName** 方法會抓取正在使用之 proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f756d-107">The **getProxyName** method retrieves the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="f756d-108">語法</span><span class="sxs-lookup"><span data-stu-id="f756d-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyName(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="f756d-109">參數</span><span class="sxs-lookup"><span data-stu-id="f756d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f756d-110">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f756d-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f756d-111">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="f756d-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="f756d-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f756d-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f756d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f756d-113">Return value</span></span>

<span data-ttu-id="f756d-114">這個方法會傳回 **字串** ，其中包含所使用之 proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f756d-114">This method returns a **String** containing the name of the proxy server being used.</span></span> <span data-ttu-id="f756d-115">只有當 **getProxySettings** 傳回的值為 2 () 使用手動設定時，傳回的值才有意義。</span><span class="sxs-lookup"><span data-stu-id="f756d-115">The value returned is meaningful only when **getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="f756d-116">備註</span><span class="sxs-lookup"><span data-stu-id="f756d-116">Remarks</span></span>

<span data-ttu-id="f756d-117">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="f756d-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="f756d-118">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f756d-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f756d-119">範例</span><span class="sxs-lookup"><span data-stu-id="f756d-119">Examples</span></span>

<span data-ttu-id="f756d-120">下列 JScript 範例會使用 *網路*。**getProxyName** ，顯示 HTTP 和 MMS 通訊協定的 Windows Media Player proxy 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f756d-120">The following JScript example uses *Network*.**getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="f756d-121">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="f756d-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

```



## <a name="requirements"></a><span data-ttu-id="f756d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f756d-122">Requirements</span></span>



| <span data-ttu-id="f756d-123">需求</span><span class="sxs-lookup"><span data-stu-id="f756d-123">Requirement</span></span> | <span data-ttu-id="f756d-124">值</span><span class="sxs-lookup"><span data-stu-id="f756d-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f756d-125">版本</span><span class="sxs-lookup"><span data-stu-id="f756d-125">Version</span></span><br/> | <span data-ttu-id="f756d-126">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f756d-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f756d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f756d-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="f756d-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f756d-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f756d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f756d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f756d-130">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="f756d-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="f756d-131">**GetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="f756d-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





