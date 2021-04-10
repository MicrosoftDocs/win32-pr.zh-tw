---
title: TaskFolder. SetSecurityDescriptor 屬性
description: 針對腳本，設定資料夾的安全描述項。
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- SetSecurityDescriptor 屬性工作排程器
- SetSecurityDescriptor 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器、SetSecurityDescriptor 屬性
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934143"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a><span data-ttu-id="1e05b-106">TaskFolder. SetSecurityDescriptor 屬性</span><span class="sxs-lookup"><span data-stu-id="1e05b-106">TaskFolder.SetSecurityDescriptor property</span></span>

<span data-ttu-id="1e05b-107">針對腳本，設定資料夾的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="1e05b-107">For scripting, sets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e05b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e05b-108">Syntax</span></span>


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a><span data-ttu-id="1e05b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1e05b-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="1e05b-110">備註</span><span class="sxs-lookup"><span data-stu-id="1e05b-110">Remarks</span></span>

<span data-ttu-id="1e05b-111">您可以在工作資料夾的安全描述項中指定存取控制清單 (ACL) ，以便允許或拒絕特定使用者和群組存取工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="1e05b-111">You can specify the access control list (ACL) in the security descriptor for a task folder in order to allow or deny certain users and groups access to a task folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e05b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e05b-112">Requirements</span></span>



| <span data-ttu-id="1e05b-113">需求</span><span class="sxs-lookup"><span data-stu-id="1e05b-113">Requirement</span></span> | <span data-ttu-id="1e05b-114">值</span><span class="sxs-lookup"><span data-stu-id="1e05b-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e05b-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e05b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1e05b-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e05b-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1e05b-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e05b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1e05b-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e05b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e05b-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1e05b-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e05b-120"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1e05b-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1e05b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1e05b-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e05b-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e05b-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e05b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e05b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e05b-124">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1e05b-124">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="1e05b-125">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1e05b-125">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





