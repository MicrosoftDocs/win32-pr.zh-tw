---
title: '其他 TSF 文字服務常數 (Ctffunc .h) '
description: 下列值適用于文字服務。
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ebd7d22f9cfbd59f95ee3dcfe68229536503b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965929"
---
# <a name="miscellaneous-tsf-text-service-constants"></a><span data-ttu-id="d0e19-103">其他 TSF 文字服務常數</span><span class="sxs-lookup"><span data-stu-id="d0e19-103">Miscellaneous TSF Text Service Constants</span></span>

<span data-ttu-id="d0e19-104">下列值適用于文字服務。</span><span class="sxs-lookup"><span data-stu-id="d0e19-104">The following values are used with text services.</span></span>



| <span data-ttu-id="d0e19-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="d0e19-105">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="d0e19-106">Description</span><span class="sxs-lookup"><span data-stu-id="d0e19-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <span data-ttu-id="d0e19-107"><dt>**TF \_MENUREADY**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d0e19-107"><dt>**TF\_MENUREADY**</dt> <dt>0x00000001</dt></span></span> </dl>                                                | <span data-ttu-id="d0e19-108">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0e19-108">Not currently used.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <span data-ttu-id="d0e19-109"><dt>**TF \_PROPUI \_ 狀態 \_ SAVETOFILE**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d0e19-109"><dt>**TF\_PROPUI\_STATUS\_SAVETOFILE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="d0e19-110">可以序列化屬性。</span><span class="sxs-lookup"><span data-stu-id="d0e19-110">The property can be serialized.</span></span> <span data-ttu-id="d0e19-111">如果此值不存在，就無法序列化屬性。</span><span class="sxs-lookup"><span data-stu-id="d0e19-111">If this value is not present, the property cannot be serialized.</span></span> <span data-ttu-id="d0e19-112">此值會搭配 [ITfFnPropertyUIStatus：： GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) 和 [ITfFnPropertyUIStatus：： SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)一起使用。</span><span class="sxs-lookup"><span data-stu-id="d0e19-112">This value is used with [ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) and [ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d0e19-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0e19-113">Requirements</span></span>



| <span data-ttu-id="d0e19-114">需求</span><span class="sxs-lookup"><span data-stu-id="d0e19-114">Requirement</span></span> | <span data-ttu-id="d0e19-115">值</span><span class="sxs-lookup"><span data-stu-id="d0e19-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e19-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0e19-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e19-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0e19-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d0e19-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0e19-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e19-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0e19-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d0e19-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d0e19-120">Redistributable</span></span><br/>          | <span data-ttu-id="d0e19-121">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="d0e19-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="d0e19-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d0e19-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0e19-123"><dt>Ctffunc。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0e19-123"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0e19-124">Idl</span><span class="sxs-lookup"><span data-stu-id="d0e19-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d0e19-125"><dt>Ctffunc .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d0e19-125"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0e19-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0e19-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e19-127">ITfFnPropertyUIStatus：： GetStatus</span><span class="sxs-lookup"><span data-stu-id="d0e19-127">ITfFnPropertyUIStatus::GetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[<span data-ttu-id="d0e19-128">ITfFnPropertyUIStatus：： SetStatus</span><span class="sxs-lookup"><span data-stu-id="d0e19-128">ITfFnPropertyUIStatus::SetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





