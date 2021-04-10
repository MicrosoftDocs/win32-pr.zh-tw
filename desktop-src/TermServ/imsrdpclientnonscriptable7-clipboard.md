---
title: IMsRdpClientNonScriptable7 剪貼簿屬性
description: 如果啟用手動剪貼簿同步，則取得用來同步處理本機和遠端寫字板的剪貼簿控制器。
ms.tgt_platform: multiple
keywords:
- 剪貼簿屬性遠端桌面服務
- 剪貼簿屬性遠端桌面服務、IMsRdpClientNonScriptable7 介面
- IMsRdpClientNonScriptable7 介面遠端桌面服務，剪貼簿屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "103935597"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a><span data-ttu-id="1cdc6-106">IMsRdpClientNonScriptable7：：剪貼簿屬性</span><span class="sxs-lookup"><span data-stu-id="1cdc6-106">IMsRdpClientNonScriptable7::Clipboard property</span></span>

<span data-ttu-id="1cdc6-107">如果啟用手動剪貼簿同步，則取得用來同步處理本機和遠端寫字板的剪貼簿控制器。</span><span class="sxs-lookup"><span data-stu-id="1cdc6-107">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>

<span data-ttu-id="1cdc6-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1cdc6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cdc6-109">語法</span><span class="sxs-lookup"><span data-stu-id="1cdc6-109">Syntax</span></span>

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a><span data-ttu-id="1cdc6-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="1cdc6-110">Property value</span></span>

<span data-ttu-id="1cdc6-111">如果啟用手動剪貼簿同步，則表示用來同步處理本機和遠端寫字板的剪貼簿控制器的 [IMsRdpClipboard](imsrdpclipboard.md) ， (也就是 [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) 屬性值設定為 **True**) 。</span><span class="sxs-lookup"><span data-stu-id="1cdc6-111">An [IMsRdpClipboard](imsrdpclipboard.md) that represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cdc6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cdc6-112">Requirements</span></span>

| <span data-ttu-id="1cdc6-113">需求</span><span class="sxs-lookup"><span data-stu-id="1cdc6-113">Requirement</span></span> | <span data-ttu-id="1cdc6-114">值</span><span class="sxs-lookup"><span data-stu-id="1cdc6-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="1cdc6-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cdc6-115">Minimum supported client</span></span>| <span data-ttu-id="1cdc6-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="1cdc6-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="1cdc6-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1cdc6-117">Type library</span></span>            | <span data-ttu-id="1cdc6-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="1cdc6-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="1cdc6-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1cdc6-119">DLL</span></span>                  | <span data-ttu-id="1cdc6-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="1cdc6-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="1cdc6-121">IID</span><span class="sxs-lookup"><span data-stu-id="1cdc6-121">IID</span></span>                      | <span data-ttu-id="1cdc6-122">IID \_ IMsRdpClientNonScriptable7 定義為71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="1cdc6-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="1cdc6-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cdc6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cdc6-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="1cdc6-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>