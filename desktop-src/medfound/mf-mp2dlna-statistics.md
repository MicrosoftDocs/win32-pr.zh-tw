---
description: 取得數位客廳網路聯盟 (DLNA) 媒體接收器的統計資料。
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: 'MF_MP2DLNA_STATISTICS 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512832"
---
# <a name="mf_mp2dlna_statistics-attribute"></a><span data-ttu-id="50a6f-103">MF \_ MP2DLNA \_ 統計資料屬性</span><span class="sxs-lookup"><span data-stu-id="50a6f-103">MF\_MP2DLNA\_STATISTICS attribute</span></span>

<span data-ttu-id="50a6f-104">取得數位客廳網路聯盟 (DLNA) 媒體接收器的統計資料。</span><span class="sxs-lookup"><span data-stu-id="50a6f-104">Gets statistics from the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="50a6f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="50a6f-105">Data type</span></span>

<span data-ttu-id="50a6f-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** 儲存為 **位元組 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="50a6f-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="50a6f-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="50a6f-107">Get/set</span></span>

<span data-ttu-id="50a6f-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="50a6f-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="50a6f-109">備註</span><span class="sxs-lookup"><span data-stu-id="50a6f-109">Remarks</span></span>

<span data-ttu-id="50a6f-110">在串流處理期間，DLNA 媒體接收器會使用 MPEG-2 資料流程的編碼和多工處理相關統計資料來更新此屬性。</span><span class="sxs-lookup"><span data-stu-id="50a6f-110">During streaming, the DLNA media sink updates this attribute with statistics about the encoding and multiplexing of the MPEG-2 streams.</span></span> <span data-ttu-id="50a6f-111">應用程式可以隨時查詢這個屬性，以取得最新的值。</span><span class="sxs-lookup"><span data-stu-id="50a6f-111">The application can query this attribute at any time to get the latest values.</span></span>

<span data-ttu-id="50a6f-112">在 DLNA 媒體接收器上設定此屬性沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="50a6f-112">Setting this attribute on the DLNA media sink has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="50a6f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="50a6f-113">Requirements</span></span>



| <span data-ttu-id="50a6f-114">需求</span><span class="sxs-lookup"><span data-stu-id="50a6f-114">Requirement</span></span> | <span data-ttu-id="50a6f-115">值</span><span class="sxs-lookup"><span data-stu-id="50a6f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50a6f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50a6f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="50a6f-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50a6f-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="50a6f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50a6f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="50a6f-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50a6f-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="50a6f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="50a6f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="50a6f-121"><dt>Mfmp2dlna。h</dt></span><span class="sxs-lookup"><span data-stu-id="50a6f-121"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50a6f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50a6f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50a6f-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="50a6f-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




