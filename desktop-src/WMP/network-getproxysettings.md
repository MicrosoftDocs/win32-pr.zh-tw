---
title: GetProxySettings 方法
description: GetProxySettings 方法會取得指定之通訊協定的 proxy 設定。
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- getProxySettings 方法 Windows Media Player
- getProxySettings 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxySettings 方法
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000810"
---
# <a name="networkgetproxysettings-method"></a><span data-ttu-id="bac1e-106">GetProxySettings 方法</span><span class="sxs-lookup"><span data-stu-id="bac1e-106">Network.getProxySettings method</span></span>

<span data-ttu-id="bac1e-107">**GetProxySettings** 方法會取得指定之通訊協定的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="bac1e-107">The **getProxySettings** method retrieves the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac1e-108">語法</span><span class="sxs-lookup"><span data-stu-id="bac1e-108">Syntax</span></span>


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="bac1e-109">參數</span><span class="sxs-lookup"><span data-stu-id="bac1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bac1e-110">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bac1e-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bac1e-111">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="bac1e-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="bac1e-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="bac1e-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bac1e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bac1e-113">Return value</span></span>

<span data-ttu-id="bac1e-114">這個方法會傳回 **數位** (**Long**) ，其中包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bac1e-114">This method returns a **Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="bac1e-115">值</span><span class="sxs-lookup"><span data-stu-id="bac1e-115">Value</span></span> | <span data-ttu-id="bac1e-116">描述</span><span class="sxs-lookup"><span data-stu-id="bac1e-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bac1e-117">0</span><span class="sxs-lookup"><span data-stu-id="bac1e-117">0</span></span>     | <span data-ttu-id="bac1e-118">未使用 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="bac1e-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="bac1e-119">1</span><span class="sxs-lookup"><span data-stu-id="bac1e-119">1</span></span>     | <span data-ttu-id="bac1e-120">目前瀏覽器的 proxy 設定正在使用中 (僅適用于 HTTP) 。</span><span class="sxs-lookup"><span data-stu-id="bac1e-120">The proxy settings for the current browser are being used (only valid for HTTP).</span></span> |
| <span data-ttu-id="bac1e-121">2</span><span class="sxs-lookup"><span data-stu-id="bac1e-121">2</span></span>     | <span data-ttu-id="bac1e-122">正在使用手動指定的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="bac1e-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="bac1e-123">3</span><span class="sxs-lookup"><span data-stu-id="bac1e-123">3</span></span>     | <span data-ttu-id="bac1e-124">系統會自動偵測到 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="bac1e-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="bac1e-125">備註</span><span class="sxs-lookup"><span data-stu-id="bac1e-125">Remarks</span></span>

<span data-ttu-id="bac1e-126">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="bac1e-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="bac1e-127">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="bac1e-127">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="bac1e-128">範例</span><span class="sxs-lookup"><span data-stu-id="bac1e-128">Examples</span></span>

<span data-ttu-id="bac1e-129">下列 JScript 範例會使用 *網路*。**getProxySettings** 顯示一則訊息，它會在瀏覽器視窗中提供播放程式目前 proxy 設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bac1e-129">The following JScript example uses *Network*.**getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in the browser window.</span></span> <span data-ttu-id="bac1e-130">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="bac1e-130">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a><span data-ttu-id="bac1e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="bac1e-131">Requirements</span></span>



| <span data-ttu-id="bac1e-132">需求</span><span class="sxs-lookup"><span data-stu-id="bac1e-132">Requirement</span></span> | <span data-ttu-id="bac1e-133">值</span><span class="sxs-lookup"><span data-stu-id="bac1e-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bac1e-134">版本</span><span class="sxs-lookup"><span data-stu-id="bac1e-134">Version</span></span><br/> | <span data-ttu-id="bac1e-135">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="bac1e-135">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bac1e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bac1e-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="bac1e-137"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bac1e-137"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bac1e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bac1e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac1e-139">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="bac1e-139">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





