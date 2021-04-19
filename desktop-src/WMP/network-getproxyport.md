---
title: GetProxyPort 方法
description: GetProxyPort 方法會抓取正在使用的 proxy 埠。
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- getProxyPort 方法 Windows Media Player
- getProxyPort 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxyPort 方法
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995672"
---
# <a name="networkgetproxyport-method"></a><span data-ttu-id="d4625-106">GetProxyPort 方法</span><span class="sxs-lookup"><span data-stu-id="d4625-106">Network.getProxyPort method</span></span>

<span data-ttu-id="d4625-107">**GetProxyPort** 方法會抓取正在使用的 proxy 埠。</span><span class="sxs-lookup"><span data-stu-id="d4625-107">The **getProxyPort** method retrieves the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4625-108">語法</span><span class="sxs-lookup"><span data-stu-id="d4625-108">Syntax</span></span>


```JScript
retVal = Network.getProxyPort(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="d4625-109">參數</span><span class="sxs-lookup"><span data-stu-id="d4625-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4625-110">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4625-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4625-111">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="d4625-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="d4625-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d4625-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4625-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4625-113">Return value</span></span>

<span data-ttu-id="d4625-114">這個方法會傳回 **數位** (**Long**) ，其中包含所使用的 proxy 埠。</span><span class="sxs-lookup"><span data-stu-id="d4625-114">This method returns a **Number** (**long**) containing the proxy port being used.</span></span> <span data-ttu-id="d4625-115">只有當 **getProxySettings** 傳回兩個 (使用手動設定) 的值時，傳回的值才有意義。</span><span class="sxs-lookup"><span data-stu-id="d4625-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4625-116">備註</span><span class="sxs-lookup"><span data-stu-id="d4625-116">Remarks</span></span>

<span data-ttu-id="d4625-117">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="d4625-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="d4625-118">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d4625-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="d4625-119">範例</span><span class="sxs-lookup"><span data-stu-id="d4625-119">Examples</span></span>

<span data-ttu-id="d4625-120">下列 JScript 範例會使用 *網路*。**getProxyPort** 可顯示 MMS 和 HTTP 通訊協定的目前 Windows Media Player proxy 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="d4625-120">The following JScript example uses *Network*.**getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="d4625-121">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="d4625-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

```



## <a name="requirements"></a><span data-ttu-id="d4625-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4625-122">Requirements</span></span>



| <span data-ttu-id="d4625-123">需求</span><span class="sxs-lookup"><span data-stu-id="d4625-123">Requirement</span></span> | <span data-ttu-id="d4625-124">值</span><span class="sxs-lookup"><span data-stu-id="d4625-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4625-125">版本</span><span class="sxs-lookup"><span data-stu-id="d4625-125">Version</span></span><br/> | <span data-ttu-id="d4625-126">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d4625-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d4625-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d4625-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4625-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4625-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4625-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4625-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4625-130">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="d4625-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="d4625-131">**GetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="d4625-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





