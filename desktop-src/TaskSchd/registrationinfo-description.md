---
title: RegistrationInfo。 Description 屬性
description: 針對腳本，取得或設定工作的描述。
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Description 屬性工作排程器
- Description 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器、Description 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c79b60fe6a96493c52011e5bd731679b3fee1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383822"
---
# <a name="registrationinfodescription-property"></a><span data-ttu-id="8bac0-106">RegistrationInfo。 Description 屬性</span><span class="sxs-lookup"><span data-stu-id="8bac0-106">RegistrationInfo.Description property</span></span>

<span data-ttu-id="8bac0-107">針對腳本，取得或設定工作的描述。</span><span class="sxs-lookup"><span data-stu-id="8bac0-107">For scripting, gets or sets the description of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bac0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bac0-108">Syntax</span></span>


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a><span data-ttu-id="8bac0-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8bac0-109">Property value</span></span>

<span data-ttu-id="8bac0-110">工作的描述。</span><span class="sxs-lookup"><span data-stu-id="8bac0-110">The description of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bac0-111">備註</span><span class="sxs-lookup"><span data-stu-id="8bac0-111">Remarks</span></span>

<span data-ttu-id="8bac0-112">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**description**](taskschedulerschema-description-registrationinfotype-element.md) 元素來指定工作的描述。</span><span class="sxs-lookup"><span data-stu-id="8bac0-112">When reading or writing XML for a task, the description of the task is specified using the [**Description**](taskschedulerschema-description-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="8bac0-113">設定這個屬性值時，值可以是從資源 .dll 檔案抓取的文字。</span><span class="sxs-lookup"><span data-stu-id="8bac0-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="8bac0-114">特製化的字串會用來參考資源檔中的文字。</span><span class="sxs-lookup"><span data-stu-id="8bac0-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="8bac0-115">字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ dll \] 是包含資源的 .Dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bac0-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="8bac0-116">例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="8bac0-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bac0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bac0-117">Requirements</span></span>



| <span data-ttu-id="8bac0-118">需求</span><span class="sxs-lookup"><span data-stu-id="8bac0-118">Requirement</span></span> | <span data-ttu-id="8bac0-119">值</span><span class="sxs-lookup"><span data-stu-id="8bac0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bac0-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bac0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8bac0-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bac0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8bac0-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bac0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8bac0-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bac0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8bac0-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8bac0-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8bac0-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8bac0-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8bac0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8bac0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bac0-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bac0-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bac0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bac0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bac0-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8bac0-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





