---
title: 'PICTYPE 常數 (OleCtl) '
description: 描述圖片取得類型所傳回的圖片物件類型，以及 \_ 描述傳遞給 OleCreatePictureIndirect 之 PICTDESC 結構的 picType 成員中的圖片類型。
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968544"
---
# <a name="pictype-constants"></a><span data-ttu-id="5a981-103">PICTYPE 常數</span><span class="sxs-lookup"><span data-stu-id="5a981-103">PICTYPE Constants</span></span>

<span data-ttu-id="5a981-104">描述 [**圖片：： get \_ 類型**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)所傳回的圖片物件類型，以及描述傳遞給 [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)之 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)結構的 **picType** 成員中的圖片類型。</span><span class="sxs-lookup"><span data-stu-id="5a981-104">Describe the type of a picture object as returned by [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), as well as to describe the type of picture in the **picType** member of the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure that is passed to [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>



| <span data-ttu-id="5a981-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="5a981-105">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="5a981-106">Description</span><span class="sxs-lookup"><span data-stu-id="5a981-106">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <span data-ttu-id="5a981-107"><dt>**PICTYPE \_未初始化**</dt><dt>的 (-1)</dt></span><span class="sxs-lookup"><span data-stu-id="5a981-107"><dt>**PICTYPE\_UNINITIALIZED**</dt> <dt>(-1)</dt></span></span> </dl> | <span data-ttu-id="5a981-108">圖片物件目前未初始化。</span><span class="sxs-lookup"><span data-stu-id="5a981-108">The picture object is currently uninitialized.</span></span> <span data-ttu-id="5a981-109">此值僅適用于 [**圖片：： get \_ 類型**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) 的傳回值，而且不能與 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構有效。</span><span class="sxs-lookup"><span data-stu-id="5a981-109">This value is only valid as a return value from [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) and is not valid with the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <span data-ttu-id="5a981-110"><dt>**PICTYPE \_無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5a981-110"><dt>**PICTYPE\_NONE**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="5a981-111">建立新的圖片物件時不會有初始化的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a981-111">A new picture object is to be created without an initialized state.</span></span> <span data-ttu-id="5a981-112">只有在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中，這個值才有效。</span><span class="sxs-lookup"><span data-stu-id="5a981-112">This value is valid only in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <span data-ttu-id="5a981-113"><dt>**PICTYPE \_點陣圖**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5a981-113"><dt>**PICTYPE\_BITMAP**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="5a981-114">圖片類型是點陣圖。</span><span class="sxs-lookup"><span data-stu-id="5a981-114">The picture type is a bitmap.</span></span> <span data-ttu-id="5a981-115">當此值發生在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中時，表示該結構的 **bmp** 欄位包含相關的初始化參數。</span><span class="sxs-lookup"><span data-stu-id="5a981-115">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **bmp** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <span data-ttu-id="5a981-116"><dt>**PICTYPE \_中繼檔**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5a981-116"><dt>**PICTYPE\_METAFILE**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="5a981-117">圖片類型為中繼檔。</span><span class="sxs-lookup"><span data-stu-id="5a981-117">The picture type is a metafile.</span></span> <span data-ttu-id="5a981-118">當此值發生在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中時，表示該結構的 **wmf** 欄位包含相關的初始化參數。</span><span class="sxs-lookup"><span data-stu-id="5a981-118">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **wmf** field of that structure contains the relevant initialization parameters.</span></span><br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <span data-ttu-id="5a981-119"><dt>**PICTYPE \_圖示**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5a981-119"><dt>**PICTYPE\_ICON**</dt> <dt>3</dt></span></span> </dl>                               | <span data-ttu-id="5a981-120">圖片類型是圖示。</span><span class="sxs-lookup"><span data-stu-id="5a981-120">The picture type is an icon.</span></span> <span data-ttu-id="5a981-121">當此值發生在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中時，表示該結構的 **圖示** 欄位包含相關的初始化參數。</span><span class="sxs-lookup"><span data-stu-id="5a981-121">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **icon** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <span data-ttu-id="5a981-122"><dt>**PICTYPE \_ENHMETAFILE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5a981-122"><dt>**PICTYPE\_ENHMETAFILE**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="5a981-123">圖片類型是增強的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="5a981-123">The picture type is an enhanced metafile.</span></span> <span data-ttu-id="5a981-124">當此值發生在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中時，表示該結構的 **emf** 欄位包含相關的初始化參數。</span><span class="sxs-lookup"><span data-stu-id="5a981-124">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **emf** field of that structure contains the relevant initialization parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5a981-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a981-125">Requirements</span></span>



| <span data-ttu-id="5a981-126">需求</span><span class="sxs-lookup"><span data-stu-id="5a981-126">Requirement</span></span> | <span data-ttu-id="5a981-127">值</span><span class="sxs-lookup"><span data-stu-id="5a981-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5a981-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a981-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5a981-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a981-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5a981-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a981-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5a981-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a981-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5a981-132">標頭</span><span class="sxs-lookup"><span data-stu-id="5a981-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a981-133"><dt>OleCtl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a981-133"><dt>OleCtl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a981-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a981-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a981-135">**圖片：： get \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="5a981-135">**IPicture::get\_Type**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[<span data-ttu-id="5a981-136">**OleCreatePictureIndirect**</span><span class="sxs-lookup"><span data-stu-id="5a981-136">**OleCreatePictureIndirect**</span></span>](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[<span data-ttu-id="5a981-137">**PICTDESC**</span><span class="sxs-lookup"><span data-stu-id="5a981-137">**PICTDESC**</span></span>](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





