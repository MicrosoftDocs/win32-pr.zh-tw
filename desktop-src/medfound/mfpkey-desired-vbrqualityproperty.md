---
description: 針對以品質為基礎 (1-通過) 可變位速率 (VBR) 編碼音訊串流，指定所需的品質等級。
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: 'MFPKEY_DESIRED_VBRQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993080"
---
# <a name="mfpkey_desired_vbrquality-property"></a><span data-ttu-id="f9845-103">MFPKEY \_ 所需的 \_ VBRQUALITY 屬性</span><span class="sxs-lookup"><span data-stu-id="f9845-103">MFPKEY\_DESIRED\_VBRQUALITY Property</span></span>

<span data-ttu-id="f9845-104">針對以品質為基礎 (1-通過) 可變位速率 (VBR) 編碼音訊串流，指定所需的品質等級。</span><span class="sxs-lookup"><span data-stu-id="f9845-104">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding of audio streams.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f9845-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="f9845-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f9845-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="f9845-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f9845-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="f9845-107">Data Type</span></span>

<span data-ttu-id="f9845-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="f9845-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="f9845-109">預設值</span><span class="sxs-lookup"><span data-stu-id="f9845-109">Default Value</span></span>

<span data-ttu-id="f9845-110">0</span><span class="sxs-lookup"><span data-stu-id="f9845-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="f9845-111">備註</span><span class="sxs-lookup"><span data-stu-id="f9845-111">Remarks</span></span>

<span data-ttu-id="f9845-112">這個值可以是0到100，其中100是最高品質。</span><span class="sxs-lookup"><span data-stu-id="f9845-112">This value can be from 0 to 100, where 100 is maximum quality.</span></span> <span data-ttu-id="f9845-113">值為0表示不使用以品質為基礎的 VBR 編碼方法。</span><span class="sxs-lookup"><span data-stu-id="f9845-113">A value of 0 indicates that the quality-based VBR encoding method is not to be used.</span></span>

<span data-ttu-id="f9845-114">若要列舉符合特定品質需求的 VBR 模式，請設定下列編碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="f9845-114">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="f9845-115">將 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f9845-115">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="f9845-116">Set [**MFPKEY \_ 將 \_ 列舉的 \_ VBRQUALITY 限制**](mfpkey-constrain-enumerated-vbrqualityproperty.md) 為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f9845-116">Set [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="f9845-117">將 **MFPKEY \_ 所需的 \_ VBRQUALITY** 設定為所需的品質。</span><span class="sxs-lookup"><span data-stu-id="f9845-117">Set **MFPKEY\_DESIRED\_VBRQUALITY** to the desired quality.</span></span> <span data-ttu-id="f9845-118">若為不失真模式，請將所需的品質設定為100。</span><span class="sxs-lookup"><span data-stu-id="f9845-118">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9845-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9845-119">Requirements</span></span>



| <span data-ttu-id="f9845-120">需求</span><span class="sxs-lookup"><span data-stu-id="f9845-120">Requirement</span></span> | <span data-ttu-id="f9845-121">值</span><span class="sxs-lookup"><span data-stu-id="f9845-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9845-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9845-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9845-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9845-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f9845-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9845-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9845-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9845-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9845-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f9845-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9845-127"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9845-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9845-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9845-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9845-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="f9845-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
