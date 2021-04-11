---
title: 'ConnectionOptions： UserName 屬性 (WSManDisp. h) '
description: 設定並取得遠端電腦上本機或網域帳戶的使用者名稱。 這個屬性會決定驗證的使用者名稱。
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- UserName 屬性 Windows 遠端管理
- UserName 屬性 Windows 遠端管理，ConnectionOptions 物件
- ConnectionOptions 物件 Windows 遠端管理，使用者名稱屬性
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104585"
---
# <a name="connectionoptionsusername-property"></a><span data-ttu-id="c6c79-107">ConnectionOptions。 UserName 屬性</span><span class="sxs-lookup"><span data-stu-id="c6c79-107">ConnectionOptions.UserName property</span></span>

<span data-ttu-id="c6c79-108">設定並取得遠端電腦上本機或網域帳戶的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="c6c79-108">Sets and gets the user name of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="c6c79-109">這個屬性會決定驗證的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="c6c79-109">This property determines the user name for authentication.</span></span> <span data-ttu-id="c6c79-110">如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md)。</span><span class="sxs-lookup"><span data-stu-id="c6c79-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="c6c79-111">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c6c79-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c79-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6c79-112">Syntax</span></span>


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a><span data-ttu-id="c6c79-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="c6c79-113">Property value</span></span>

<span data-ttu-id="c6c79-114">包含遠端電腦上本機或網域帳戶之使用者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="c6c79-114">String that contains the user name of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="c6c79-115">如果未提供任何值，且未設定 **WSManFlagCredUsernamePassword** 旗標，則會使用執行腳本之帳戶的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="c6c79-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the user name of the account that is running the script is used.</span></span>

<span data-ttu-id="c6c79-116">如果未提供任何值，且已設定 **WSManFlagCredUsernamePassword** 旗標，則腳本會提示使用者輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="c6c79-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the user name and password.</span></span> <span data-ttu-id="c6c79-117">如果未輸入有效的使用者名稱和密碼，則會傳回拒絕存取錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6c79-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c79-118">備註</span><span class="sxs-lookup"><span data-stu-id="c6c79-118">Remarks</span></span>

<span data-ttu-id="c6c79-119">下列語法用來指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="c6c79-119">The following syntax is used to specify this property.</span></span>


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



<span data-ttu-id="c6c79-120">使用 [*negotiate*](windows-remote-management-glossary.md)或 *Kerberos* 驗證時，您可以提供網域帳戶的使用者 **名稱** 和 [**密碼**](connectionoptions-password.md)，或使用 [*基本*](windows-remote-management-glossary.md)身份驗證的本機帳戶。</span><span class="sxs-lookup"><span data-stu-id="c6c79-120">You can supply **UserName** and [**Password**](connectionoptions-password.md) for a domain account when using [*negotiate*](windows-remote-management-glossary.md) or *Kerberos* authentication, or for a local account with [*Basic*](windows-remote-management-glossary.md) authentication.</span></span> <span data-ttu-id="c6c79-121">若要連接到本機帳戶， [**CreateSession**](wsman-createsession.md) 旗標必須包含 **WSManFlagUseBasic** 旗標和 **WsmanFlagCredUserNamePassword** 旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="c6c79-121">To connect to a local account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseBasic** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="c6c79-122">若要連接到網域帳戶， **CreateSession** 旗標必須包含 **WSManFlagUseNegotiate** 旗標和 **WsmanFlagCredUserNamePassword** 旗標的組合，或是 **WSManFlagUseKerberos** 旗標和 **WsmanFlagCredUserNamePassword** 旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="c6c79-122">To connect to a domain account, the **WSMan.CreateSession** flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag, or the combination of the **WSManFlagUseKerberos** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="c6c79-123">網域帳戶的使用者名稱 **必須以** 「電腦使用者名稱」格式指定 \\ ，其中「電腦」部分的字串可以是名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c6c79-123">For a domain account, **UserName** must be specified in the form "computer\\username", where the "computer" part of the string can be either the name or the IP address.</span></span> <span data-ttu-id="c6c79-124">如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md)。</span><span class="sxs-lookup"><span data-stu-id="c6c79-124">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



<span data-ttu-id="c6c79-125">若要連接到網域帳戶， [**CreateSession**](wsman-createsession.md) 旗標必須包含 **WSManFlagUseNegotiate** 旗標和 **WsmanFlagCredUserNamePassword** 旗標的組合，以連接到需要協商驗證的網域帳戶。</span><span class="sxs-lookup"><span data-stu-id="c6c79-125">For connecting to a domain account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag for connecting to a domain account, which requires Negotiate authentication.</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



## <a name="requirements"></a><span data-ttu-id="c6c79-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6c79-126">Requirements</span></span>



| <span data-ttu-id="c6c79-127">需求</span><span class="sxs-lookup"><span data-stu-id="c6c79-127">Requirement</span></span> | <span data-ttu-id="c6c79-128">值</span><span class="sxs-lookup"><span data-stu-id="c6c79-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c79-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6c79-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c79-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6c79-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c6c79-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6c79-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c79-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6c79-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c6c79-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c6c79-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c79-134"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c79-134"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6c79-135">Idl</span><span class="sxs-lookup"><span data-stu-id="c6c79-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6c79-136"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6c79-136"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c6c79-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="c6c79-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6c79-138"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c6c79-138"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c6c79-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c6c79-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6c79-140"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6c79-140"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c6c79-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6c79-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c79-142">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="c6c79-142">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





