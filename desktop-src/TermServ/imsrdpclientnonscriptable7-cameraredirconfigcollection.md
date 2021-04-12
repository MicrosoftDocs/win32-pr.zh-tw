---
title: IMsRdpClientNonScriptable7 CameraRedirConfigCollection 屬性
description: 取得 (的攝影機集合，以及可用於重新導向的相關聯設定) 。
ms.tgt_platform: multiple
keywords:
- CameraRedirConfigCollection 屬性遠端桌面服務
- CameraRedirConfigCollection 屬性遠端桌面服務，IMsRdpClientNonScriptable7 介面
- IMsRdpClientNonScriptable7 介面遠端桌面服務，CameraRedirConfigCollection 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104317535"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a><span data-ttu-id="9232e-106">IMsRdpClientNonScriptable7：： CameraRedirConfigCollection 屬性</span><span class="sxs-lookup"><span data-stu-id="9232e-106">IMsRdpClientNonScriptable7::CameraRedirConfigCollection property</span></span>

<span data-ttu-id="9232e-107">取得 (的攝影機集合，以及可用於重新導向的相關聯設定) 。</span><span class="sxs-lookup"><span data-stu-id="9232e-107">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

<span data-ttu-id="9232e-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9232e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9232e-109">語法</span><span class="sxs-lookup"><span data-stu-id="9232e-109">Syntax</span></span>


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a><span data-ttu-id="9232e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9232e-110">Property value</span></span>

<span data-ttu-id="9232e-111">[IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) ，表示 (的相機集合，以及可供重新導向的相關聯設定) 。</span><span class="sxs-lookup"><span data-stu-id="9232e-111">An [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) that represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="9232e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9232e-112">Requirements</span></span>

| <span data-ttu-id="9232e-113">需求</span><span class="sxs-lookup"><span data-stu-id="9232e-113">Requirement</span></span> | <span data-ttu-id="9232e-114">值</span><span class="sxs-lookup"><span data-stu-id="9232e-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="9232e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9232e-115">Minimum supported client</span></span>| <span data-ttu-id="9232e-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="9232e-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="9232e-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9232e-117">Type library</span></span>            | <span data-ttu-id="9232e-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9232e-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="9232e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9232e-119">DLL</span></span>                  | <span data-ttu-id="9232e-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9232e-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="9232e-121">IID</span><span class="sxs-lookup"><span data-stu-id="9232e-121">IID</span></span>                      | <span data-ttu-id="9232e-122">IID \_ IMsRdpClientNonScriptable7 定義為71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="9232e-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="9232e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9232e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9232e-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="9232e-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>