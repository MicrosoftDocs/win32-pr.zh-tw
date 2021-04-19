---
title: SetProxySettings 方法
description: SetProxySettings 方法會為指定的通訊協定指定 proxy 設定。
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- setProxySettings 方法 Windows Media Player
- setProxySettings 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxySettings 方法
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984292"
---
# <a name="networksetproxysettings-method"></a><span data-ttu-id="67aa8-106">SetProxySettings 方法</span><span class="sxs-lookup"><span data-stu-id="67aa8-106">Network.setProxySettings method</span></span>

<span data-ttu-id="67aa8-107">**SetProxySettings** 方法會為指定的通訊協定指定 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="67aa8-107">The **setProxySettings** method specifies the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="67aa8-108">語法</span><span class="sxs-lookup"><span data-stu-id="67aa8-108">Syntax</span></span>


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a><span data-ttu-id="67aa8-109">參數</span><span class="sxs-lookup"><span data-stu-id="67aa8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67aa8-110">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67aa8-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67aa8-111">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="67aa8-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="67aa8-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="67aa8-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="67aa8-113">*設定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67aa8-113">*setting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67aa8-114">包含下列其中一個值的 (**long**) **數位**。</span><span class="sxs-lookup"><span data-stu-id="67aa8-114">**Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="67aa8-115">值</span><span class="sxs-lookup"><span data-stu-id="67aa8-115">Value</span></span> | <span data-ttu-id="67aa8-116">描述</span><span class="sxs-lookup"><span data-stu-id="67aa8-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="67aa8-117">0</span><span class="sxs-lookup"><span data-stu-id="67aa8-117">0</span></span>     | <span data-ttu-id="67aa8-118">不使用 Proxy 伺服器：</span><span class="sxs-lookup"><span data-stu-id="67aa8-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="67aa8-119">1</span><span class="sxs-lookup"><span data-stu-id="67aa8-119">1</span></span>     | <span data-ttu-id="67aa8-120">使用目前瀏覽器的 proxy 設定 (僅適用于 HTTP) 。</span><span class="sxs-lookup"><span data-stu-id="67aa8-120">Use the proxy settings of the current browser (only valid for HTTP).</span></span> |
| <span data-ttu-id="67aa8-121">2</span><span class="sxs-lookup"><span data-stu-id="67aa8-121">2</span></span>     | <span data-ttu-id="67aa8-122">使用手動指定的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="67aa8-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="67aa8-123">3</span><span class="sxs-lookup"><span data-stu-id="67aa8-123">3</span></span>     | <span data-ttu-id="67aa8-124">自動偵測 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="67aa8-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67aa8-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="67aa8-125">Return value</span></span>

<span data-ttu-id="67aa8-126">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="67aa8-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67aa8-127">備註</span><span class="sxs-lookup"><span data-stu-id="67aa8-127">Remarks</span></span>

<span data-ttu-id="67aa8-128">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="67aa8-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="67aa8-129">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="67aa8-129">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="67aa8-130">範例</span><span class="sxs-lookup"><span data-stu-id="67aa8-130">Examples</span></span>

<span data-ttu-id="67aa8-131">下列範例會使用 JScript 搭配 HTML SELECT **元素，以允許使用者指定 HTTP 通訊協定的 Windows Media Player proxy 設定。** 使用 ID = "player" 建立 player 物件。</span><span class="sxs-lookup"><span data-stu-id="67aa8-131">The following example uses JScript with an HTML SELECT **element to allow the user to specify the Windows Media Player proxy setting for the HTTP protocol. The Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="67aa8-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="67aa8-132">Requirements</span></span>



| <span data-ttu-id="67aa8-133">需求</span><span class="sxs-lookup"><span data-stu-id="67aa8-133">Requirement</span></span> | <span data-ttu-id="67aa8-134">值</span><span class="sxs-lookup"><span data-stu-id="67aa8-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67aa8-135">版本</span><span class="sxs-lookup"><span data-stu-id="67aa8-135">Version</span></span><br/> | <span data-ttu-id="67aa8-136">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="67aa8-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="67aa8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="67aa8-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="67aa8-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67aa8-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67aa8-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67aa8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67aa8-140">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="67aa8-140">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





