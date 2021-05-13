---
description: 將非預設磁片配額指派給新的使用者。
title: DiskQuotaControl. AddUser 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841529"
---
# <a name="diskquotacontroladduser-method"></a><span data-ttu-id="db79d-103">DiskQuotaControl. AddUser 方法</span><span class="sxs-lookup"><span data-stu-id="db79d-103">DiskQuotaControl.AddUser method</span></span>

<span data-ttu-id="db79d-104">將非預設磁片配額指派給新的使用者。</span><span class="sxs-lookup"><span data-stu-id="db79d-104">Assigns a nondefault disk quota to a new user.</span></span>

## <a name="syntax"></a><span data-ttu-id="db79d-105">語法</span><span class="sxs-lookup"><span data-stu-id="db79d-105">Syntax</span></span>


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="db79d-106">參數</span><span class="sxs-lookup"><span data-stu-id="db79d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db79d-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="db79d-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="db79d-108">類型： **CHAR**</span><span class="sxs-lookup"><span data-stu-id="db79d-108">Type: **CHAR**</span></span>

<span data-ttu-id="db79d-109">包含使用者登入名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="db79d-109">A string value that contains the user's logon name.</span></span> <span data-ttu-id="db79d-110">您可以使用 [**UserNameResolution**](diskquotacontrol-usernameresolution.md) 屬性來指定名稱的解析方式。</span><span class="sxs-lookup"><span data-stu-id="db79d-110">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to specify how the name is to be resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db79d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="db79d-111">Return value</span></span>

<span data-ttu-id="db79d-112">Type： **Object**</span><span class="sxs-lookup"><span data-stu-id="db79d-112">Type: **Object**</span></span>

<span data-ttu-id="db79d-113">傳回評估為使用者 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的物件運算式。</span><span class="sxs-lookup"><span data-stu-id="db79d-113">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="db79d-114">備註</span><span class="sxs-lookup"><span data-stu-id="db79d-114">Remarks</span></span>

<span data-ttu-id="db79d-115">當使用者第一次寫入磁片區時，NTFS 檔案系統會自動建立使用者配額專案。</span><span class="sxs-lookup"><span data-stu-id="db79d-115">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="db79d-116">以這種方式建立的專案，會獲指派預設的警告臨界值和磁片區的固定配額限制值。</span><span class="sxs-lookup"><span data-stu-id="db79d-116">Entries that are created in this way are assigned the default warning threshold and hard quota limit values for the volume.</span></span> <span data-ttu-id="db79d-117">此方法可讓您在使用者將資訊寫入磁片區之前，建立使用者配額專案。</span><span class="sxs-lookup"><span data-stu-id="db79d-117">This method allows you to create a user quota entry before a user writes information to the volume.</span></span> <span data-ttu-id="db79d-118">它會傳回 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件，這個物件可用來指派與磁片區的預設設定不同的警告臨界值或配額限制值。</span><span class="sxs-lookup"><span data-stu-id="db79d-118">It returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to assign a warning threshold or quota limit value that differs from the default settings for the volume.</span></span>

<span data-ttu-id="db79d-119">如果使用者已經存在，則不會建立新專案。</span><span class="sxs-lookup"><span data-stu-id="db79d-119">If the user already exists, no new entry is created.</span></span> <span data-ttu-id="db79d-120">方法會傳回與現有專案相關聯的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="db79d-120">The method returns the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the existing entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="db79d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="db79d-121">Requirements</span></span>



| <span data-ttu-id="db79d-122">需求</span><span class="sxs-lookup"><span data-stu-id="db79d-122">Requirement</span></span> | <span data-ttu-id="db79d-123">值</span><span class="sxs-lookup"><span data-stu-id="db79d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db79d-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db79d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="db79d-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db79d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db79d-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db79d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="db79d-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db79d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="db79d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="db79d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db79d-129"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="db79d-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db79d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db79d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db79d-131">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="db79d-131">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="db79d-132">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="db79d-132">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="db79d-133">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="db79d-133">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




