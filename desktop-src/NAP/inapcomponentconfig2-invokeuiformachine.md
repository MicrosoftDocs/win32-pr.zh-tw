---
title: 'INapComponentConfig2 InvokeUIForMachine 方法 (NapCommon .h) '
description: 由系統健康狀態驗證 (Shv) 視需要在指定的電腦上直接管理遠端設定。 這個方法會啟動設定管理 UI。
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- InvokeUIForMachine 方法 NAP
- InvokeUIForMachine 方法 NAP，INapComponentConfig2 介面
- INapComponentConfig2 介面 NAP，InvokeUIForMachine 方法
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094488"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a><span data-ttu-id="9de27-107">INapComponentConfig2：： InvokeUIForMachine 方法</span><span class="sxs-lookup"><span data-stu-id="9de27-107">INapComponentConfig2::InvokeUIForMachine method</span></span>

> [!Note]  
> <span data-ttu-id="9de27-108">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="9de27-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9de27-109">**InvokeUIForMachine** 方法是由系統健康狀態驗證 (shv) 視需要在指定的電腦上直接管理遠端設定。</span><span class="sxs-lookup"><span data-stu-id="9de27-109">The **InvokeUIForMachine** method is implemented by system health validators (SHVs) as needed to manage remote configuration directly on the machine specified.</span></span> <span data-ttu-id="9de27-110">這個方法會啟動設定管理 UI。</span><span class="sxs-lookup"><span data-stu-id="9de27-110">This method launches a configuration management UI.</span></span>

## <a name="syntax"></a><span data-ttu-id="9de27-111">語法</span><span class="sxs-lookup"><span data-stu-id="9de27-111">Syntax</span></span>


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a><span data-ttu-id="9de27-112">參數</span><span class="sxs-lookup"><span data-stu-id="9de27-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de27-113">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9de27-113">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de27-114">父系或擁有者視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9de27-114">A handle to the parent or owner window.</span></span> <span data-ttu-id="9de27-115">必須提供有效的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="9de27-115">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="9de27-116">*machineName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9de27-116">*machineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de27-117">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)的指標，其中包含 NAP 用戶端的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="9de27-117">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de27-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="9de27-118">Return value</span></span>

<span data-ttu-id="9de27-119">\_如果成功或其中一個標準 Windows 錯誤碼，則會傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="9de27-119">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9de27-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9de27-120">Requirements</span></span>



| <span data-ttu-id="9de27-121">需求</span><span class="sxs-lookup"><span data-stu-id="9de27-121">Requirement</span></span> | <span data-ttu-id="9de27-122">值</span><span class="sxs-lookup"><span data-stu-id="9de27-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9de27-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9de27-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9de27-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="9de27-124">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9de27-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9de27-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9de27-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9de27-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9de27-127">標頭</span><span class="sxs-lookup"><span data-stu-id="9de27-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de27-128"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="9de27-128"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="9de27-129">Idl</span><span class="sxs-lookup"><span data-stu-id="9de27-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9de27-130"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9de27-130"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de27-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9de27-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de27-132">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="9de27-132">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





