---
title: RegistrationInfo. 作者屬性
description: 針對腳本，取得或設定工作的作者。
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- 作者屬性工作排程器
- Author 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器，作者屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Author
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7e940ff9da2cfccaa306ebf73080da2a28a091
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024546"
---
# <a name="registrationinfoauthor-property"></a><span data-ttu-id="eb142-106">RegistrationInfo. 作者屬性</span><span class="sxs-lookup"><span data-stu-id="eb142-106">RegistrationInfo.Author property</span></span>

<span data-ttu-id="eb142-107">針對腳本，取得或設定工作的作者。</span><span class="sxs-lookup"><span data-stu-id="eb142-107">For scripting, gets or sets the author of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb142-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb142-108">Syntax</span></span>


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a><span data-ttu-id="eb142-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="eb142-109">Property value</span></span>

<span data-ttu-id="eb142-110">工作的作者。</span><span class="sxs-lookup"><span data-stu-id="eb142-110">The author of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb142-111">備註</span><span class="sxs-lookup"><span data-stu-id="eb142-111">Remarks</span></span>

<span data-ttu-id="eb142-112">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**author**](taskschedulerschema-author-registrationinfotype-element.md) 元素來指定工作作者。</span><span class="sxs-lookup"><span data-stu-id="eb142-112">When reading or writing XML for a task, the task author is specified using the [**Author**](taskschedulerschema-author-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="eb142-113">設定這個屬性值時，值可以是從資源 .dll 檔案抓取的文字。</span><span class="sxs-lookup"><span data-stu-id="eb142-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="eb142-114">特製化的字串會用來參考資源檔中的文字。</span><span class="sxs-lookup"><span data-stu-id="eb142-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="eb142-115">字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ dll \] 是包含資源的 .Dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb142-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="eb142-116">例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="eb142-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb142-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb142-117">Requirements</span></span>



| <span data-ttu-id="eb142-118">需求</span><span class="sxs-lookup"><span data-stu-id="eb142-118">Requirement</span></span> | <span data-ttu-id="eb142-119">值</span><span class="sxs-lookup"><span data-stu-id="eb142-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb142-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb142-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eb142-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb142-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="eb142-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb142-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eb142-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb142-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb142-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="eb142-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb142-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb142-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb142-126">DLL</span><span class="sxs-lookup"><span data-stu-id="eb142-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb142-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb142-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb142-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb142-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb142-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="eb142-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





