---
title: 'GUID_COMPARTMENT_TRANSITORYEXTENSION (Ctffunc 的值) '
description: 下列 GUID 區間 TRANSITORYEXTENSION 區間的 \_ 值 \_ 可用來控制暫時性擴充功能的行為。
ms.assetid: a81a18be-fb71-4414-a552-3ae2582349f9
keywords:
- GUID_COMPARTMENT_TRANSITORYEXTENSION 文字服務架構的值
topic_type:
- apiref
api_name:
- Values for GUID_COMPARTMENT_TRANSITORYEXTENSION
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef92f2fe043c51596eb1bb7484f242925daa3c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465641"
---
# <a name="values-for-guid_compartment_transitoryextension"></a><span data-ttu-id="d8347-104">GUID 區間 TRANSITORYEXTENSION 的值 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d8347-104">Values for GUID\_COMPARTMENT\_TRANSITORYEXTENSION</span></span>

<span data-ttu-id="d8347-105">下列 GUID 區間 TRANSITORYEXTENSION 區間的 \_ 值 \_ 可用來控制暫時性擴充功能的行為。</span><span class="sxs-lookup"><span data-stu-id="d8347-105">The following values of the GUID\_COMPARTMENT\_TRANSITORYEXTENSION compartment are used to control the behavior of transitory extension.</span></span>

<dl> <dt>

<span data-ttu-id="d8347-106"><span id="TF_TRANSITORYEXTENSION_NONE"></span><span id="tf_transitoryextension_none"></span>**TF \_ TRANSITORYEXTENSION \_ NONE**</span><span class="sxs-lookup"><span data-stu-id="d8347-106"><span id="TF_TRANSITORYEXTENSION_NONE"></span><span id="tf_transitoryextension_none"></span>**TF\_TRANSITORYEXTENSION\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="d8347-107">此值會停止暫時性延伸模組。</span><span class="sxs-lookup"><span data-stu-id="d8347-107">This value stops the transitory extension.</span></span>

</dd> <dt>

<span data-ttu-id="d8347-108"><span id="TF_TRANSITORYEXTENSION_FLOATING"></span><span id="tf_transitoryextension_floating"></span>**TF \_ TRANSITORYEXTENSION \_ 浮動**</span><span class="sxs-lookup"><span data-stu-id="d8347-108"><span id="TF_TRANSITORYEXTENSION_FLOATING"></span><span id="tf_transitoryextension_floating"></span>**TF\_TRANSITORYEXTENSION\_FLOATING**</span></span>
</dt> <dd>

<span data-ttu-id="d8347-109">此值會以浮動 UI 啟動暫時性延伸模組。</span><span class="sxs-lookup"><span data-stu-id="d8347-109">This value starts the transitory extension with the floating UI.</span></span>

</dd> <dt>

<span data-ttu-id="d8347-110"><span id="TF_TRANSITORYEXTENSION_ATSELECTION"></span><span id="tf_transitoryextension_atselection"></span>**TF \_ TRANSITORYEXTENSION \_ ATSELECTION**</span><span class="sxs-lookup"><span data-stu-id="d8347-110"><span id="TF_TRANSITORYEXTENSION_ATSELECTION"></span><span id="tf_transitoryextension_atselection"></span>**TF\_TRANSITORYEXTENSION\_ATSELECTION**</span></span>
</dt> <dd>

<span data-ttu-id="d8347-111">這個值會使用位於 IP 或父檔管理員選取範圍的快顯視窗 UI 來啟動暫時性延伸。</span><span class="sxs-lookup"><span data-stu-id="d8347-111">This value starts the transitory extension with the popup UI at the IP or the selection of the parent document manager.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8347-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8347-112">Requirements</span></span>



| <span data-ttu-id="d8347-113">需求</span><span class="sxs-lookup"><span data-stu-id="d8347-113">Requirement</span></span> | <span data-ttu-id="d8347-114">值</span><span class="sxs-lookup"><span data-stu-id="d8347-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8347-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8347-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d8347-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8347-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8347-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8347-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d8347-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8347-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d8347-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d8347-119">Redistributable</span></span><br/>          | <span data-ttu-id="d8347-120">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="d8347-120">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="d8347-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d8347-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8347-122"><dt>Ctffunc。h</dt></span><span class="sxs-lookup"><span data-stu-id="d8347-122"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8347-123">Idl</span><span class="sxs-lookup"><span data-stu-id="d8347-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8347-124"><dt>Ctffunc .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8347-124"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8347-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8347-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8347-126">預先定義的區間</span><span class="sxs-lookup"><span data-stu-id="d8347-126">Predefined Compartments</span></span>](predefined-compartments.md)
</dt> </dl>

 

 





