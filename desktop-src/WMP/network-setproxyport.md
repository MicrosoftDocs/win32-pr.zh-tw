---
title: SetProxyPort 方法
description: SetProxyPort 方法會指定要使用的 proxy 埠。 |SetProxyPort 方法
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- setProxyPort 方法 Windows Media Player
- setProxyPort 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxyPort 方法
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993940"
---
# <a name="networksetproxyport-method"></a><span data-ttu-id="d3970-107">SetProxyPort 方法</span><span class="sxs-lookup"><span data-stu-id="d3970-107">Network.setProxyPort method</span></span>

<span data-ttu-id="d3970-108">**SetProxyPort** 方法會指定要使用的 proxy 埠。</span><span class="sxs-lookup"><span data-stu-id="d3970-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3970-109">語法</span><span class="sxs-lookup"><span data-stu-id="d3970-109">Syntax</span></span>


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a><span data-ttu-id="d3970-110">參數</span><span class="sxs-lookup"><span data-stu-id="d3970-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3970-111">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3970-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3970-112">指定通訊協定名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="d3970-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="d3970-113">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d3970-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3970-114">*埠* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3970-114">*port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3970-115"> (**long**) 指定要使用的 Proxy 埠 **數目**。</span><span class="sxs-lookup"><span data-stu-id="d3970-115">**Number** (**long**) specifying the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3970-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3970-116">Return value</span></span>

<span data-ttu-id="d3970-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d3970-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3970-118">備註</span><span class="sxs-lookup"><span data-stu-id="d3970-118">Remarks</span></span>

<span data-ttu-id="d3970-119">除非 **getProxySettings** 傳回值 2 () 使用手動設定，否則這個方法沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="d3970-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="d3970-120">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="d3970-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="d3970-121">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d3970-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="d3970-122">範例</span><span class="sxs-lookup"><span data-stu-id="d3970-122">Examples</span></span>

<span data-ttu-id="d3970-123">下列 JScript 範例會使用 *網路*。**setProxyPort** 指定 MMS 通訊協定的 Windows Media Player proxy 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="d3970-123">The following JScript example uses *Network*.**setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="d3970-124">埠號碼是從 ID = "PORT" 的 HTML INPUT 元素取出。</span><span class="sxs-lookup"><span data-stu-id="d3970-124">The port number is retrieved from an HTML INPUT element with ID = "PORT".</span></span> <span data-ttu-id="d3970-125">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="d3970-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="d3970-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3970-126">Requirements</span></span>



| <span data-ttu-id="d3970-127">需求</span><span class="sxs-lookup"><span data-stu-id="d3970-127">Requirement</span></span> | <span data-ttu-id="d3970-128">值</span><span class="sxs-lookup"><span data-stu-id="d3970-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3970-129">版本</span><span class="sxs-lookup"><span data-stu-id="d3970-129">Version</span></span><br/> | <span data-ttu-id="d3970-130">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d3970-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d3970-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d3970-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="d3970-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3970-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3970-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3970-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3970-134">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="d3970-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





