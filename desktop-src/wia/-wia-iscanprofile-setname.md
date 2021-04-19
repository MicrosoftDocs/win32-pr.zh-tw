---
description: 設定設定檔的易記名稱。
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'IScanProfile：： SetName 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977921"
---
# <a name="iscanprofilesetname-method"></a><span data-ttu-id="c3072-103">IScanProfile：： SetName 方法</span><span class="sxs-lookup"><span data-stu-id="c3072-103">IScanProfile::SetName method</span></span>

<span data-ttu-id="c3072-104">設定設定檔的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c3072-104">Sets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3072-105">語法</span><span class="sxs-lookup"><span data-stu-id="c3072-105">Syntax</span></span>


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a><span data-ttu-id="c3072-106">參數</span><span class="sxs-lookup"><span data-stu-id="c3072-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3072-107">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3072-107">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3072-108">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c3072-108">Type: **BSTR**</span></span>

<span data-ttu-id="c3072-109">設定檔的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c3072-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3072-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3072-110">Return value</span></span>

<span data-ttu-id="c3072-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c3072-111">Type: **HRESULT**</span></span>

<span data-ttu-id="c3072-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c3072-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c3072-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c3072-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3072-114">備註</span><span class="sxs-lookup"><span data-stu-id="c3072-114">Remarks</span></span>

<span data-ttu-id="c3072-115">這個方法是必要的，因為設定檔的 GUID 不能用來向使用者顯示掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="c3072-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

<span data-ttu-id="c3072-116">使用者可以使用 [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法來變更設定檔的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c3072-116">A user can change the friendly name of a profile with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="c3072-117">設定檔的變更不會儲存到磁片，直到應用程式呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法為止。</span><span class="sxs-lookup"><span data-stu-id="c3072-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="c3072-118">如果兩個應用程式會從相同的 XML 檔案建立掃描設定檔物件，而且每個應用程式都會將變更寫入其物件，則只有呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) last 的應用程式所做的變更會儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="c3072-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3072-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3072-119">Requirements</span></span>



| <span data-ttu-id="c3072-120">需求</span><span class="sxs-lookup"><span data-stu-id="c3072-120">Requirement</span></span> | <span data-ttu-id="c3072-121">值</span><span class="sxs-lookup"><span data-stu-id="c3072-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3072-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3072-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3072-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3072-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c3072-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3072-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3072-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3072-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3072-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c3072-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3072-127"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3072-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="c3072-128">Idl</span><span class="sxs-lookup"><span data-stu-id="c3072-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c3072-129"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3072-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



 

 




