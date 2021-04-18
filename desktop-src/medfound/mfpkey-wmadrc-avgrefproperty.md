---
description: 指定音訊內容的平均音量層級。
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: 'MFPKEY_WMADRC_AVGREF 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983377"
---
# <a name="mfpkey_wmadrc_avgref-property"></a><span data-ttu-id="c1cfe-103">MFPKEY \_ WMADRC \_ AVGREF 屬性</span><span class="sxs-lookup"><span data-stu-id="c1cfe-103">MFPKEY\_WMADRC\_AVGREF Property</span></span>

<span data-ttu-id="c1cfe-104">指定音訊內容的平均音量層級。</span><span class="sxs-lookup"><span data-stu-id="c1cfe-104">Specifies the average volume level of audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c1cfe-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="c1cfe-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c1cfe-106">g \_ wszWMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="c1cfe-106">g\_wszWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="c1cfe-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="c1cfe-107">Data Type</span></span>

<span data-ttu-id="c1cfe-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c1cfe-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="c1cfe-109">備註</span><span class="sxs-lookup"><span data-stu-id="c1cfe-109">Remarks</span></span>

<span data-ttu-id="c1cfe-110">處理內容之後，您可以從編碼器取得此值。</span><span class="sxs-lookup"><span data-stu-id="c1cfe-110">You can get this value from the encoder after the content is processed.</span></span> <span data-ttu-id="c1cfe-111">您也可以在解碼器上設定此值以用於動態範圍控制項，但只有在已設定 [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) 屬性時，才會有作用。</span><span class="sxs-lookup"><span data-stu-id="c1cfe-111">This value can also be set on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="c1cfe-112">如需動態範圍控制項的詳細資訊，請參閱 web 文章 [Windows Media 音訊 Professional 編解碼器功能](/previous-versions/ms867218(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="c1cfe-112">For more information on dynamic range control see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1cfe-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1cfe-113">Requirements</span></span>



| <span data-ttu-id="c1cfe-114">需求</span><span class="sxs-lookup"><span data-stu-id="c1cfe-114">Requirement</span></span> | <span data-ttu-id="c1cfe-115">值</span><span class="sxs-lookup"><span data-stu-id="c1cfe-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cfe-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1cfe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cfe-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1cfe-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c1cfe-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1cfe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cfe-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1cfe-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1cfe-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c1cfe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1cfe-121"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1cfe-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1cfe-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1cfe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1cfe-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="c1cfe-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
