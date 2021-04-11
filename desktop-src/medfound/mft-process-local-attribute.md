---
description: 指定是否僅在應用程式處理常式中註冊媒體基礎轉換 (MFT) 。
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: 'MFT_PROCESS_LOCAL_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691648"
---
# <a name="mft_process_local_attribute-attribute"></a><span data-ttu-id="18742-103">MFT \_ 進程 \_ 區域 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="18742-103">MFT\_PROCESS\_LOCAL\_Attribute attribute</span></span>

<span data-ttu-id="18742-104">指定是否只在應用程式的進程中註冊媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="18742-104">Specifies whether a Media Foundation transform (MFT) is registered only in the application's process.</span></span>

## <a name="data-type"></a><span data-ttu-id="18742-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="18742-105">Data type</span></span>

<span data-ttu-id="18742-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="18742-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="18742-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="18742-107">Get/set</span></span>

<span data-ttu-id="18742-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="18742-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="18742-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="18742-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="18742-110">備註</span><span class="sxs-lookup"><span data-stu-id="18742-110">Remarks</span></span>

<span data-ttu-id="18742-111">這個屬性的使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="18742-111">This attribute is used as follows:</span></span>

1.  <span data-ttu-id="18742-112">應用程式會藉由呼叫 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) 或 [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) 函式來註冊本機 MFT。</span><span class="sxs-lookup"><span data-stu-id="18742-112">The application registers a local MFT by calling either the [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) function.</span></span> <span data-ttu-id="18742-113">這些函式會在應用程式的進程中註冊 MFT。</span><span class="sxs-lookup"><span data-stu-id="18742-113">These functions register the MFT in the application's process.</span></span>
2.  <span data-ttu-id="18742-114">呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數，以列舉符合一組特定準則的 MFTs。</span><span class="sxs-lookup"><span data-stu-id="18742-114">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function is called to enumerate MFTs that match a particular set of criteria.</span></span> <span data-ttu-id="18742-115">應用程式可能會直接呼叫 **MFTEnumEx** 函式，但較常由拓撲載入器呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="18742-115">The application might call the **MFTEnumEx** function directly, but more often this function is called by the topology loader.</span></span>
3.  <span data-ttu-id="18742-116">[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式會捕獲 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標的陣列，每個指標都代表一個 MFT 的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="18742-116">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function retrieves an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each representing an activation object for an MFT.</span></span> <span data-ttu-id="18742-117">如果在本機註冊了 MFT，則 \_ 對應的啟用物件上的 [mft 進程 \_ 區域屬性] \_ 屬性會設定為 [ **TRUE** ]。</span><span class="sxs-lookup"><span data-stu-id="18742-117">If an MFT is registered locally, the MFT\_PROCESS\_LOCAL\_Attribute attribute is set to **TRUE** on the corresponding activation object.</span></span>

<span data-ttu-id="18742-118">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="18742-118">The default value for this attribute is **FALSE**.</span></span>

<span data-ttu-id="18742-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="18742-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="18742-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="18742-120">Requirements</span></span>



| <span data-ttu-id="18742-121">需求</span><span class="sxs-lookup"><span data-stu-id="18742-121">Requirement</span></span> | <span data-ttu-id="18742-122">值</span><span class="sxs-lookup"><span data-stu-id="18742-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18742-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18742-123">Minimum supported client</span></span><br/> | <span data-ttu-id="18742-124">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18742-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="18742-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18742-125">Minimum supported server</span></span><br/> | <span data-ttu-id="18742-126">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18742-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="18742-127">標頭</span><span class="sxs-lookup"><span data-stu-id="18742-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="18742-128"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="18742-128"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18742-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18742-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18742-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="18742-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18742-131">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="18742-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




