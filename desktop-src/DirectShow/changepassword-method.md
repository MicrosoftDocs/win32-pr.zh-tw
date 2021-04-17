---
description: DVDAdm 方法會在登錄中儲存新的應用程式密碼。
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467519"
---
# <a name="changepassword-method"></a><span data-ttu-id="f32fc-103">ChangePassword 方法</span><span class="sxs-lookup"><span data-stu-id="f32fc-103">ChangePassword Method</span></span>

> [!Note]  
> <span data-ttu-id="f32fc-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="f32fc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f32fc-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f32fc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f32fc-106">方法會將 `DVDAdm.ChangePassword` 新的應用程式密碼儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="f32fc-106">The `DVDAdm.ChangePassword` method saves a new application password in the registry.</span></span>

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a><span data-ttu-id="f32fc-107">參數</span><span class="sxs-lookup"><span data-stu-id="f32fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f32fc-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="f32fc-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="f32fc-109">將目前使用者的登入名稱指定為字串。</span><span class="sxs-lookup"><span data-stu-id="f32fc-109">Specifies the current user's logon name as a String.</span></span> <span data-ttu-id="f32fc-110">MSDVDAdm 物件會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="f32fc-110">The MSDVDAdm object ignores this parameter.</span></span> <span data-ttu-id="f32fc-111">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f32fc-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f32fc-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*出售*</span><span class="sxs-lookup"><span data-stu-id="f32fc-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*sOld*</span></span>
</dt> <dd>

<span data-ttu-id="f32fc-113">將使用者的舊密碼指定為字串。</span><span class="sxs-lookup"><span data-stu-id="f32fc-113">Specifies the user's old password as a String.</span></span>

</dd> <dt>

<span data-ttu-id="f32fc-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span><span class="sxs-lookup"><span data-stu-id="f32fc-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span></span>
</dt> <dd>

<span data-ttu-id="f32fc-115">將使用者的新密碼指定為字串。</span><span class="sxs-lookup"><span data-stu-id="f32fc-115">Specifies the user's new password as a String.</span></span> <span data-ttu-id="f32fc-116">不能是空字串。</span><span class="sxs-lookup"><span data-stu-id="f32fc-116">Cannot be an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f32fc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f32fc-117">Return Value</span></span>

<span data-ttu-id="f32fc-118">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="f32fc-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f32fc-119">備註</span><span class="sxs-lookup"><span data-stu-id="f32fc-119">Remarks</span></span>

<span data-ttu-id="f32fc-120">目前，這個和所有相關的方法會忽略 *sUserName* 參數。</span><span class="sxs-lookup"><span data-stu-id="f32fc-120">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span> <span data-ttu-id="f32fc-121">這表示任何知道密碼的人都可以設定家長的層級。</span><span class="sxs-lookup"><span data-stu-id="f32fc-121">This means that whoever knows the password can set the parental level.</span></span> <span data-ttu-id="f32fc-122">應用程式只有一個密碼和一個家長層級。</span><span class="sxs-lookup"><span data-stu-id="f32fc-122">There is only one password and one parental level for the application.</span></span> <span data-ttu-id="f32fc-123">不支援個別使用者登入名稱或多重密碼管理。</span><span class="sxs-lookup"><span data-stu-id="f32fc-123">There is no support for individual user logon names or multiple password management.</span></span> <span data-ttu-id="f32fc-124">若要強制執行家長管理層級，家長應設定密碼，然後為親屬群組的年輕成員設定適當的家長監護層級。</span><span class="sxs-lookup"><span data-stu-id="f32fc-124">To enforce parental management levels, parents should set the password and then set the parental level appropriate for younger members of the group of relatives.</span></span> <span data-ttu-id="f32fc-125">當家長想要查看具有成人分級內容的光碟時，他們可以變更層級，然後在完成觀看時將其變更回來。</span><span class="sxs-lookup"><span data-stu-id="f32fc-125">When parents want to view a disc with adult-rated content, they can change the level, and then change it back when they are done viewing.</span></span> <span data-ttu-id="f32fc-126">只要子系不知道密碼，他們就只能在其設定的層級或下方監看內容。</span><span class="sxs-lookup"><span data-stu-id="f32fc-126">As long as the children do not know the password, they can only watch content at or below the level set for them.</span></span>

## <a name="see-also"></a><span data-ttu-id="f32fc-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f32fc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32fc-128">**ConfirmPassword**</span><span class="sxs-lookup"><span data-stu-id="f32fc-128">**ConfirmPassword**</span></span>](confirmpassword-method.md)
</dt> <dt>

[<span data-ttu-id="f32fc-129">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="f32fc-129">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



