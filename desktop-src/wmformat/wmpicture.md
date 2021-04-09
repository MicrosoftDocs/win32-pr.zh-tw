---
title: WM/圖片
description: WM/圖片屬性包含與內容相關的圖片。
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- WM/Picture windows 媒體格式
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932692"
---
# <a name="wmpicture"></a><span data-ttu-id="14646-104">WM/圖片</span><span class="sxs-lookup"><span data-stu-id="14646-104">WM/Picture</span></span>

<span data-ttu-id="14646-105">**WM/圖片** 屬性包含與內容相關的圖片。</span><span class="sxs-lookup"><span data-stu-id="14646-105">The **WM/Picture** attribute contains a picture related to the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="14646-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="14646-106">Global Constant</span></span>

<span data-ttu-id="14646-107">g \_ wszWMPicture</span><span class="sxs-lookup"><span data-stu-id="14646-107">g\_wszWMPicture</span></span>

## <a name="data-type"></a><span data-ttu-id="14646-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="14646-108">Data Type</span></span>

<span data-ttu-id="14646-109">[**WM \_圖片**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT \_ 類型 \_ BINARY**) </span><span class="sxs-lookup"><span data-stu-id="14646-109">[**WM\_PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="14646-110">備註</span><span class="sxs-lookup"><span data-stu-id="14646-110">Remarks</span></span>

<span data-ttu-id="14646-111">這個屬性與 ID3 框架（APIC）相容。</span><span class="sxs-lookup"><span data-stu-id="14646-111">This attribute is compatible with the ID3 frame, APIC.</span></span> <span data-ttu-id="14646-112">APIC 框架的 ID3 規格規定，雖然可能有任意數目的 APIC 框架與檔案相關聯，但只有一個類型可以是1，而且只有一個類型是2。</span><span class="sxs-lookup"><span data-stu-id="14646-112">The ID3 specification for the APIC frame stipulates that, while there may be any number of APIC frames associated with a file, only one may be of type 1 and only one may be of type 2.</span></span> <span data-ttu-id="14646-113">規格也會指出圖片描述的長度不能超過64個字元，但可以是空的。</span><span class="sxs-lookup"><span data-stu-id="14646-113">The specification also states that the description of the picture can be no longer than 64 characters, but can be empty.</span></span>

<span data-ttu-id="14646-114">使用 Windows Media 格式 SDK 的物件新增的 WM/圖片屬性不會自動進行驗證，以符合 ID3 規格。</span><span class="sxs-lookup"><span data-stu-id="14646-114">WM/Picture attributes added with the objects of the Windows Media Format SDK are not automatically validated to conform to ID3 specifications.</span></span> <span data-ttu-id="14646-115">如果您想要維持與 ID3 的完整相容性，您必須在應用程式中加入程式碼以執行驗證。</span><span class="sxs-lookup"><span data-stu-id="14646-115">You must add code in your application to perform validations if you want to maintain complete compatibility with ID3.</span></span>

## <a name="see-also"></a><span data-ttu-id="14646-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14646-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14646-117">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="14646-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="14646-118">**WM \_ 圖片**</span><span class="sxs-lookup"><span data-stu-id="14646-118">**WM\_PICTURE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




