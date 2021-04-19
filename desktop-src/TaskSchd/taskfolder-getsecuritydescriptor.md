---
title: TaskFolder. GetSecurityDescriptor 屬性
description: 針對腳本，取得資料夾的安全描述項。
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- GetSecurityDescriptor 屬性工作排程器
- GetSecurityDescriptor 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器、GetSecurityDescriptor 屬性
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969801"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a><span data-ttu-id="b008f-106">TaskFolder. GetSecurityDescriptor 屬性</span><span class="sxs-lookup"><span data-stu-id="b008f-106">TaskFolder.GetSecurityDescriptor property</span></span>

<span data-ttu-id="b008f-107">針對腳本，取得資料夾的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b008f-107">For scripting, gets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="b008f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b008f-108">Syntax</span></span>


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a><span data-ttu-id="b008f-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="b008f-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="b008f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="b008f-110">Requirements</span></span>



| <span data-ttu-id="b008f-111">需求</span><span class="sxs-lookup"><span data-stu-id="b008f-111">Requirement</span></span> | <span data-ttu-id="b008f-112">值</span><span class="sxs-lookup"><span data-stu-id="b008f-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b008f-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b008f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b008f-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b008f-114">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b008f-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b008f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b008f-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b008f-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b008f-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b008f-117">Type library</span></span><br/>             | <dl> <span data-ttu-id="b008f-118"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b008f-118"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b008f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="b008f-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b008f-120"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b008f-120"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b008f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b008f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b008f-122">**TaskFolder.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b008f-122">**TaskFolder.SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="b008f-123">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b008f-123">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





