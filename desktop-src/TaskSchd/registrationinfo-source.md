---
title: RegistrationInfo。 Source 屬性
description: 針對腳本，取得或設定工作源自的位置。 例如，工作可能源自元件、服務、應用程式或使用者。
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Source 屬性工作排程器
- Source 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器、Source 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686143"
---
# <a name="registrationinfosource-property"></a><span data-ttu-id="5afec-107">RegistrationInfo。 Source 屬性</span><span class="sxs-lookup"><span data-stu-id="5afec-107">RegistrationInfo.Source property</span></span>

<span data-ttu-id="5afec-108">針對腳本，取得或設定工作源自的位置。</span><span class="sxs-lookup"><span data-stu-id="5afec-108">For scripting, gets or sets where the task originated from.</span></span> <span data-ttu-id="5afec-109">例如，工作可能源自元件、服務、應用程式或使用者。</span><span class="sxs-lookup"><span data-stu-id="5afec-109">For example, a task may originate from a component, service, application, or user.</span></span>

## <a name="syntax"></a><span data-ttu-id="5afec-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5afec-110">Syntax</span></span>


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a><span data-ttu-id="5afec-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="5afec-111">Property value</span></span>

<span data-ttu-id="5afec-112">工作源自的位置。</span><span class="sxs-lookup"><span data-stu-id="5afec-112">Where the task originated from.</span></span> <span data-ttu-id="5afec-113">例如，從元件、服務、應用程式或使用者。</span><span class="sxs-lookup"><span data-stu-id="5afec-113">For example, from a component, service, application, or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="5afec-114">備註</span><span class="sxs-lookup"><span data-stu-id="5afec-114">Remarks</span></span>

<span data-ttu-id="5afec-115">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**source**](taskschedulerschema-source-registrationinfotype-element.md) 元素來指定工作來源資訊。</span><span class="sxs-lookup"><span data-stu-id="5afec-115">When reading or writing XML for a task, the task source information is specified using the [**Source**](taskschedulerschema-source-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="5afec-116">設定這個屬性值時，值可以是從資源 .dll 檔案抓取的文字。</span><span class="sxs-lookup"><span data-stu-id="5afec-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="5afec-117">特製化的字串會用來參考資源檔中的文字。</span><span class="sxs-lookup"><span data-stu-id="5afec-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="5afec-118">字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ dll \] 是包含資源的 .Dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5afec-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="5afec-119">例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="5afec-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="5afec-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5afec-120">Requirements</span></span>



| <span data-ttu-id="5afec-121">需求</span><span class="sxs-lookup"><span data-stu-id="5afec-121">Requirement</span></span> | <span data-ttu-id="5afec-122">值</span><span class="sxs-lookup"><span data-stu-id="5afec-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5afec-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5afec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5afec-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5afec-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5afec-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5afec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5afec-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5afec-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5afec-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5afec-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="5afec-128"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5afec-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5afec-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5afec-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5afec-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5afec-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5afec-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5afec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5afec-132">工作排程器</span><span class="sxs-lookup"><span data-stu-id="5afec-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





