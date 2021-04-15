---
title: 'ConnectionOptions，Password 屬性 (WSManDisp. h) '
description: 設定遠端電腦上的本機或網域帳戶的密碼。 這個屬性會決定驗證的密碼。
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Password 屬性 Windows 遠端管理
- Password 屬性 Windows 遠端管理，ConnectionOptions 物件
- ConnectionOptions 物件 Windows 遠端管理，Password 屬性
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104586"
---
# <a name="connectionoptionspassword-property"></a><span data-ttu-id="f43aa-107">ConnectionOptions，Password 屬性</span><span class="sxs-lookup"><span data-stu-id="f43aa-107">ConnectionOptions.Password property</span></span>

<span data-ttu-id="f43aa-108">設定遠端電腦上的本機或網域帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="f43aa-108">Sets the password of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="f43aa-109">這個屬性會決定驗證的密碼。</span><span class="sxs-lookup"><span data-stu-id="f43aa-109">This property determines the password for authentication.</span></span> <span data-ttu-id="f43aa-110">如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md)。</span><span class="sxs-lookup"><span data-stu-id="f43aa-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="f43aa-111">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f43aa-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f43aa-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f43aa-112">Syntax</span></span>


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a><span data-ttu-id="f43aa-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="f43aa-113">Property value</span></span>

<span data-ttu-id="f43aa-114">字串，其中包含遠端電腦上的本機或網域帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="f43aa-114">String that contains the password of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="f43aa-115">如果未提供任何值，且未設定 **WSManFlagCredUsernamePassword** 旗標，則會使用執行腳本之帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="f43aa-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the password of the account that is running the script is used.</span></span>

<span data-ttu-id="f43aa-116">如果未提供任何值，且已設定 **WSManFlagCredUsernamePassword** 旗標，則腳本會提示使用者輸入密碼 (和使用者名稱（如果未提供) ）。</span><span class="sxs-lookup"><span data-stu-id="f43aa-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the password (and the user name, if this is not supplied).</span></span> <span data-ttu-id="f43aa-117">如果未輸入有效的使用者名稱和密碼，則會傳回拒絕存取錯誤。</span><span class="sxs-lookup"><span data-stu-id="f43aa-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="f43aa-118">備註</span><span class="sxs-lookup"><span data-stu-id="f43aa-118">Remarks</span></span>

<span data-ttu-id="f43aa-119">請注意，您無法取得密碼。</span><span class="sxs-lookup"><span data-stu-id="f43aa-119">Be aware that you cannot retrieve the password.</span></span> <span data-ttu-id="f43aa-120">密碼只能使用這個屬性來設定。</span><span class="sxs-lookup"><span data-stu-id="f43aa-120">The password can only be set with this property.</span></span>

<span data-ttu-id="f43aa-121">如果您建立 [**ConnectionOptions**](connectionoptions.md)物件，並使用使用者名稱和密碼連接到 Windows 遠端管理，則應該在對 [**WSMan. CreateSession**](wsman-createsession.md)的呼叫上設定 **WSManFlagCredUserNamePassword** 旗標。</span><span class="sxs-lookup"><span data-stu-id="f43aa-121">If you create a [**ConnectionOptions**](connectionoptions.md) object and use a user name and password to connect to Windows Remote Management, then the **WSManFlagCredUserNamePassword** flag should be set on the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

<span data-ttu-id="f43aa-122">如需設定密碼的詳細資訊，請參閱 [**ConnectionOptions**](connectionoptions.md)中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="f43aa-122">For more information about setting passwords, see the Remarks section in [**ConnectionOptions**](connectionoptions.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f43aa-123">範例</span><span class="sxs-lookup"><span data-stu-id="f43aa-123">Examples</span></span>

<span data-ttu-id="f43aa-124">下列程式碼範例會建立 [**ConnectionOptions**](connectionoptions.md) 物件並設定 **密碼**。</span><span class="sxs-lookup"><span data-stu-id="f43aa-124">The following code example creates a [**ConnectionOptions**](connectionoptions.md) object and sets the **Password**.</span></span>


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a><span data-ttu-id="f43aa-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f43aa-125">Requirements</span></span>



| <span data-ttu-id="f43aa-126">需求</span><span class="sxs-lookup"><span data-stu-id="f43aa-126">Requirement</span></span> | <span data-ttu-id="f43aa-127">值</span><span class="sxs-lookup"><span data-stu-id="f43aa-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f43aa-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f43aa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f43aa-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f43aa-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f43aa-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f43aa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f43aa-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f43aa-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f43aa-132">標頭</span><span class="sxs-lookup"><span data-stu-id="f43aa-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f43aa-133"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f43aa-133"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f43aa-134">Idl</span><span class="sxs-lookup"><span data-stu-id="f43aa-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f43aa-135"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f43aa-135"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f43aa-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="f43aa-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="f43aa-137"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f43aa-137"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f43aa-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f43aa-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f43aa-139"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f43aa-139"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f43aa-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f43aa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f43aa-141">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="f43aa-141">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





