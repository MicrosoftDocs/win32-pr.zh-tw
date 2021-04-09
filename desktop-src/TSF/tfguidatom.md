---
title: 'TfGuidAtom (Msctf) '
description: TfGuidAtom 資料類型會識別 TSF 內的 GUID。 TfGuidAtom 是藉由呼叫 ITfCategoryMgr RegisterGUID 所取得。
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- TfGuidAtom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093776"
---
# <a name="tfguidatom"></a><span data-ttu-id="cba86-105">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="cba86-105">TfGuidAtom</span></span>

<span data-ttu-id="cba86-106">**TfGuidAtom** 資料類型會識別 TSF 內的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="cba86-106">The **TfGuidAtom** data type identifies a **GUID** within TSF.</span></span> <span data-ttu-id="cba86-107">藉由呼叫 [**ITfCategoryMgr：： RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)，即可取得 **TfGuidAtom** 。</span><span class="sxs-lookup"><span data-stu-id="cba86-107">A **TfGuidAtom** is obtained by calling [**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a><span data-ttu-id="cba86-108">備註</span><span class="sxs-lookup"><span data-stu-id="cba86-108">Remarks</span></span>

<span data-ttu-id="cba86-109">只有在呼叫 **ITfCategoryMgr：： RegisterGUID** 的進程內， **TfGuidAtom** 值才有效。</span><span class="sxs-lookup"><span data-stu-id="cba86-109">A **TfGuidAtom** value is only valid within the process that **ITfCategoryMgr::RegisterGUID** is called from.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba86-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="cba86-110">Requirements</span></span>



| <span data-ttu-id="cba86-111">需求</span><span class="sxs-lookup"><span data-stu-id="cba86-111">Requirement</span></span> | <span data-ttu-id="cba86-112">值</span><span class="sxs-lookup"><span data-stu-id="cba86-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cba86-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cba86-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cba86-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cba86-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cba86-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cba86-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cba86-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cba86-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cba86-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="cba86-117">Redistributable</span></span><br/>          | <span data-ttu-id="cba86-118">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="cba86-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="cba86-119">標頭</span><span class="sxs-lookup"><span data-stu-id="cba86-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cba86-120"><dt>Msctf。h</dt></span><span class="sxs-lookup"><span data-stu-id="cba86-120"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="cba86-121">Idl</span><span class="sxs-lookup"><span data-stu-id="cba86-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cba86-122"><dt>Msctf .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cba86-122"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba86-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cba86-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba86-124">**ITfCategoryMgr：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="cba86-124">**ITfCategoryMgr::GetGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="cba86-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span><span class="sxs-lookup"><span data-stu-id="cba86-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[<span data-ttu-id="cba86-126">**ITfCategoryMgr::RegisterGUID**</span><span class="sxs-lookup"><span data-stu-id="cba86-126">**ITfCategoryMgr::RegisterGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





