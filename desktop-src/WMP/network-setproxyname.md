---
title: SetProxyName 方法
description: SetProxyName 方法會指定要使用的 proxy 伺服器名稱。 |SetProxyName 方法
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- setProxyName 方法 Windows Media Player
- setProxyName 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxyName 方法
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994127"
---
# <a name="networksetproxyname-method"></a><span data-ttu-id="d64a5-107">SetProxyName 方法</span><span class="sxs-lookup"><span data-stu-id="d64a5-107">Network.setProxyName method</span></span>

<span data-ttu-id="d64a5-108">**SetProxyName** 方法會指定要使用的 proxy 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d64a5-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="d64a5-109">語法</span><span class="sxs-lookup"><span data-stu-id="d64a5-109">Syntax</span></span>


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="d64a5-110">參數</span><span class="sxs-lookup"><span data-stu-id="d64a5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d64a5-111">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d64a5-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d64a5-112">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="d64a5-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="d64a5-113">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d64a5-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="d64a5-114">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d64a5-114">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d64a5-115">**字串** ，指定要使用的 proxy 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d64a5-115">**String** specifying the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d64a5-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d64a5-116">Return value</span></span>

<span data-ttu-id="d64a5-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d64a5-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d64a5-118">備註</span><span class="sxs-lookup"><span data-stu-id="d64a5-118">Remarks</span></span>

<span data-ttu-id="d64a5-119">除非 **getProxySettings** 傳回值 2 () 使用手動設定，否則這個方法沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="d64a5-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="d64a5-120">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="d64a5-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="d64a5-121">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d64a5-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="d64a5-122">範例</span><span class="sxs-lookup"><span data-stu-id="d64a5-122">Examples</span></span>

<span data-ttu-id="d64a5-123">下列 JScript 範例會使用 *網路*。**setProxyName** 指定 MMS 通訊協定 Windows Media Player proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d64a5-123">The following JScript example uses *Network*.**setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="d64a5-124">新名稱會從 ID = "NAME" 的 HTML 文字元素中取出。</span><span class="sxs-lookup"><span data-stu-id="d64a5-124">The new name is retrieved from an HTML TEXT element with ID = "NAME".</span></span> <span data-ttu-id="d64a5-125">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="d64a5-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="d64a5-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d64a5-126">Requirements</span></span>



| <span data-ttu-id="d64a5-127">需求</span><span class="sxs-lookup"><span data-stu-id="d64a5-127">Requirement</span></span> | <span data-ttu-id="d64a5-128">值</span><span class="sxs-lookup"><span data-stu-id="d64a5-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d64a5-129">版本</span><span class="sxs-lookup"><span data-stu-id="d64a5-129">Version</span></span><br/> | <span data-ttu-id="d64a5-130">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d64a5-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d64a5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d64a5-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="d64a5-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d64a5-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d64a5-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d64a5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d64a5-134">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="d64a5-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





