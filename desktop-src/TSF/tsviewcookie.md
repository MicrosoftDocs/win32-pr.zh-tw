---
title: 'TsViewCookie (Textstor) '
description: TsViewCookie 資料類型會識別內容視圖。
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106994974"
---
# <a name="tsviewcookie"></a><span data-ttu-id="c3a8a-104">TsViewCookie</span><span class="sxs-lookup"><span data-stu-id="c3a8a-104">TsViewCookie</span></span>

<span data-ttu-id="c3a8a-105">**TsViewCookie** 資料類型會識別內容視圖。</span><span class="sxs-lookup"><span data-stu-id="c3a8a-105">The **TsViewCookie** data type identifies a context view.</span></span>


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a><span data-ttu-id="c3a8a-106">備註</span><span class="sxs-lookup"><span data-stu-id="c3a8a-106">Remarks</span></span>

<span data-ttu-id="c3a8a-107">應用程式必須為其所建立的每個視圖提供唯一的 **TsViewCookie** 值。</span><span class="sxs-lookup"><span data-stu-id="c3a8a-107">An application must supply a unique **TsViewCookie** value for each view it creates.</span></span>

<span data-ttu-id="c3a8a-108">TSF 管理員會藉由呼叫 [ITextStoreACP：： GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) 或 [ITextStoreAnchor：： GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)，從應用程式取得這個值。</span><span class="sxs-lookup"><span data-stu-id="c3a8a-108">The TSF manager obtains this value from the application by calling [ITextStoreACP::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) or [ITextStoreAnchor::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span></span> <span data-ttu-id="c3a8a-109">TSF 管理員會在呼叫各種 [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) 或 [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) 方法時，使用這個值來識別此視圖。</span><span class="sxs-lookup"><span data-stu-id="c3a8a-109">The TSF manager uses this value to identify the view when calling various [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) or [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a8a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3a8a-110">Requirements</span></span>



| <span data-ttu-id="c3a8a-111">需求</span><span class="sxs-lookup"><span data-stu-id="c3a8a-111">Requirement</span></span> | <span data-ttu-id="c3a8a-112">值</span><span class="sxs-lookup"><span data-stu-id="c3a8a-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a8a-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3a8a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a8a-114">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3a8a-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="c3a8a-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3a8a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a8a-116">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3a8a-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="c3a8a-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c3a8a-117">Redistributable</span></span><br/>          | <span data-ttu-id="c3a8a-118">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="c3a8a-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="c3a8a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c3a8a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3a8a-120"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3a8a-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3a8a-121">Idl</span><span class="sxs-lookup"><span data-stu-id="c3a8a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c3a8a-122"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3a8a-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a8a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3a8a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a8a-124">**ITextStoreACP**</span><span class="sxs-lookup"><span data-stu-id="c3a8a-124">**ITextStoreACP**</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="c3a8a-125">**ITextStoreACP：： GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="c3a8a-125">**ITextStoreACP::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[<span data-ttu-id="c3a8a-126">**ITextStoreAnchor::GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="c3a8a-126">**ITextStoreAnchor::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





