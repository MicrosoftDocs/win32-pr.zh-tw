---
title: ClientSpec 列舉
description: 搭配 ClientProtocolSpec 屬性使用，以指定用戶端與伺服器之間使用的遠端桌面通訊協定。
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- ClientSpec 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966910"
---
# <a name="clientspec-enumeration"></a><span data-ttu-id="d4f8e-104">ClientSpec 列舉</span><span class="sxs-lookup"><span data-stu-id="d4f8e-104">ClientSpec enumeration</span></span>

<span data-ttu-id="d4f8e-105">搭配 [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) 屬性使用，以指定用戶端與伺服器之間使用的遠端桌面通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d4f8e-105">Used with the [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) property to specify the remote desktop protocol used between the client and the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f8e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4f8e-106">Syntax</span></span>


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a><span data-ttu-id="d4f8e-107">常數</span><span class="sxs-lookup"><span data-stu-id="d4f8e-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d4f8e-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span><span class="sxs-lookup"><span data-stu-id="d4f8e-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span></span>
</dt> <dd>

<span data-ttu-id="d4f8e-109">通訊協定已完整 Windows 8 遠端桌面通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d4f8e-109">The protocol is full Windows 8 Remote Desktop protocol.</span></span>

</dd> <dt>

<span data-ttu-id="d4f8e-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span><span class="sxs-lookup"><span data-stu-id="d4f8e-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span></span>
</dt> <dd>

<span data-ttu-id="d4f8e-111">此通訊協定僅限於使用 Windows 7 SP1 RemoteFX 編解碼器和較小的快取。</span><span class="sxs-lookup"><span data-stu-id="d4f8e-111">The protocol is limited to using the Windows 7 with SP1 RemoteFX codec and a smaller cache.</span></span> <span data-ttu-id="d4f8e-112">所有其他編解碼器皆已停用。</span><span class="sxs-lookup"><span data-stu-id="d4f8e-112">All other codecs are disabled.</span></span> <span data-ttu-id="d4f8e-113">此通訊協定具有最小的記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="d4f8e-113">This protocol has the smallest memory footprint.</span></span>

</dd> <dt>

<span data-ttu-id="d4f8e-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span><span class="sxs-lookup"><span data-stu-id="d4f8e-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span></span>
</dt> <dd>

<span data-ttu-id="d4f8e-115">通訊協定與 **FullMode** 相同，但它使用較小的快取。</span><span class="sxs-lookup"><span data-stu-id="d4f8e-115">The protocol is the same as **FullMode**, except it uses a smaller cache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4f8e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4f8e-116">Requirements</span></span>



| <span data-ttu-id="d4f8e-117">需求</span><span class="sxs-lookup"><span data-stu-id="d4f8e-117">Requirement</span></span> | <span data-ttu-id="d4f8e-118">值</span><span class="sxs-lookup"><span data-stu-id="d4f8e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f8e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4f8e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f8e-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d4f8e-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="d4f8e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4f8e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f8e-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4f8e-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="d4f8e-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d4f8e-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4f8e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4f8e-124"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4f8e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4f8e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f8e-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span><span class="sxs-lookup"><span data-stu-id="d4f8e-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span></span>](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





