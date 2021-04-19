---
description: 指定拓撲節點的基礎物件是否為 decrypter。
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: 'MF_TOPONODE_DECRYPTOR 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987368"
---
# <a name="mf_toponode_decryptor-attribute"></a><span data-ttu-id="fee73-103">MF \_ TOPONODE \_ 解密器屬性</span><span class="sxs-lookup"><span data-stu-id="fee73-103">MF\_TOPONODE\_DECRYPTOR attribute</span></span>

<span data-ttu-id="fee73-104">指定拓撲節點的基礎物件是否為 decrypter。</span><span class="sxs-lookup"><span data-stu-id="fee73-104">Specifies whether a toplogy node's underlying object is a decrypter.</span></span>

## <a name="data-type"></a><span data-ttu-id="fee73-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="fee73-105">Data type</span></span>

<span data-ttu-id="fee73-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fee73-106">**UINT32**</span></span>

<span data-ttu-id="fee73-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="fee73-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fee73-108">備註</span><span class="sxs-lookup"><span data-stu-id="fee73-108">Remarks</span></span>

<span data-ttu-id="fee73-109">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="fee73-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="fee73-110">如果這個屬性的值為非零值，則節點的基礎物件為 decrypter。</span><span class="sxs-lookup"><span data-stu-id="fee73-110">If the value of this attribute is nonzero, the node's underlying object is a decrypter.</span></span>

<span data-ttu-id="fee73-111">應用程式通常不會直接使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="fee73-111">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="fee73-112">當媒體會話建立 decrypter 的節點時，會設定這個屬性，從 [**IMFInputTrustAuthority：： GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) 方法取得。</span><span class="sxs-lookup"><span data-stu-id="fee73-112">The Media Session sets this attribute when it creates a node for a decrypter, obtained from the [**IMFInputTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) method.</span></span>

<span data-ttu-id="fee73-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="fee73-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee73-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fee73-114">Requirements</span></span>



| <span data-ttu-id="fee73-115">需求</span><span class="sxs-lookup"><span data-stu-id="fee73-115">Requirement</span></span> | <span data-ttu-id="fee73-116">值</span><span class="sxs-lookup"><span data-stu-id="fee73-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fee73-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fee73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fee73-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fee73-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fee73-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fee73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fee73-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fee73-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fee73-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fee73-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fee73-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fee73-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fee73-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fee73-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee73-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="fee73-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fee73-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="fee73-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="fee73-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="fee73-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="fee73-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="fee73-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="fee73-128">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="fee73-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




