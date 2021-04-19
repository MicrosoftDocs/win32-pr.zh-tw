---
title: ExtendedDisconnectReasonCode 列舉
description: 定義控制項中斷連接原因的延伸資訊。
ms.assetid: E73E73B4-6C6B-4270-A1BD-947FA6D7B31B
ms.tgt_platform: multiple
keywords:
- ExtendedDisconnectReasonCode 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- ExtendedDisconnectReasonCode
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657d0faee03ca37b9a5a49b95b978a24b0c8955c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965943"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a><span data-ttu-id="4632c-104">ExtendedDisconnectReasonCode 列舉</span><span class="sxs-lookup"><span data-stu-id="4632c-104">ExtendedDisconnectReasonCode enumeration</span></span>

<span data-ttu-id="4632c-105">定義控制項中斷連接原因的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="4632c-105">Defines extended information about the control's reason for disconnection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4632c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4632c-106">Syntax</span></span>


```C++
typedef enum _ExtendedDisconnectReasonCode { 
  exDiscReasonNoInfo                            = 0,
  exDiscReasonAPIInitiatedDisconnect            = 1,
  exDiscReasonAPIInitiatedLogoff                = 2,
  exDiscReasonServerIdleTimeout                 = 3,
  exDiscReasonServerLogonTimeout                = 4,
  exDiscReasonReplacedByOtherConnection         = 5,
  exDiscReasonOutOfMemory                       = 6,
  exDiscReasonServerDeniedConnection            = 7,
  exDiscReasonServerDeniedConnectionFips        = 8,
  exDiscReasonServerInsufficientPrivileges      = 9,
  exDiscReasonServerFreshCredsRequired          = 10,
  exDiscReasonRpcInitiatedDisconnectByUser      = 11,
  exDiscReasonLogoffByUser                      = 2,
  exDiscReasonLicenseInternal                   = 256,
  exDiscReasonLicenseNoLicenseServer            = 257,
  exDiscReasonLicenseNoLicense                  = 258,
  exDiscReasonLicenseErrClientMsg               = 259,
  exDiscReasonLicenseHwidDoesntMatchLicense     = 260,
  exDiscReasonLicenseErrClientLicense           = 261,
  exDiscReasonLicenseCantFinishProtocol         = 262,
  exDiscReasonLicenseClientEndedProtocol        = 263,
  exDiscReasonLicenseErrClientEncryption        = 264,
  exDiscReasonLicenseCantUpgradeLicense         = 265,
  exDiscReasonLicenseNoRemoteConnections        = 266,
  exDiscReasonLicenseCreatingLicStoreAccDenied  = 267,
  exDiscReasonRdpEncInvalidCredentials          = 768,
  exDiscReasonProtocolRangeStart                = 4096,
  exDiscReasonProtocolRangeEnd                  = 32767
} ExtendedDisconnectReasonCode;
```



## <a name="constants"></a><span data-ttu-id="4632c-107">常數</span><span class="sxs-lookup"><span data-stu-id="4632c-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4632c-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span><span class="sxs-lookup"><span data-stu-id="4632c-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-109">沒有其他資訊可用。</span><span class="sxs-lookup"><span data-stu-id="4632c-109">No additional information is available.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span><span class="sxs-lookup"><span data-stu-id="4632c-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-111">應用程式起始中斷連接。</span><span class="sxs-lookup"><span data-stu-id="4632c-111">An application initiated the disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span><span class="sxs-lookup"><span data-stu-id="4632c-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-113">登出用戶端的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4632c-113">An application logged off the client.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="4632c-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-115">伺服器已中斷用戶端的連線，因為用戶端已閒置一段時間，超過指定的超時時間。</span><span class="sxs-lookup"><span data-stu-id="4632c-115">The server has disconnected the client because the client has been idle for a period of time longer than the designated time-out period.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span><span class="sxs-lookup"><span data-stu-id="4632c-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-117">伺服器已中斷用戶端的連線，因為用戶端已超過指定的連接期間。</span><span class="sxs-lookup"><span data-stu-id="4632c-117">The server has disconnected the client because the client has exceeded the period designated for connection.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span><span class="sxs-lookup"><span data-stu-id="4632c-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-119">用戶端的連線已由另一個連接取代。</span><span class="sxs-lookup"><span data-stu-id="4632c-119">The client's connection was replaced by another connection.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span><span class="sxs-lookup"><span data-stu-id="4632c-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-121">沒有可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4632c-121">No memory is available.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span><span class="sxs-lookup"><span data-stu-id="4632c-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-123">伺服器拒絕了連接。</span><span class="sxs-lookup"><span data-stu-id="4632c-123">The server denied the connection.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span><span class="sxs-lookup"><span data-stu-id="4632c-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-125">基於安全性考慮，伺服器拒絕了連接。</span><span class="sxs-lookup"><span data-stu-id="4632c-125">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span><span class="sxs-lookup"><span data-stu-id="4632c-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-127">基於安全性考慮，伺服器拒絕了連接。</span><span class="sxs-lookup"><span data-stu-id="4632c-127">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span><span class="sxs-lookup"><span data-stu-id="4632c-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-129">需要新的認證。</span><span class="sxs-lookup"><span data-stu-id="4632c-129">Fresh credentials are required.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span><span class="sxs-lookup"><span data-stu-id="4632c-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-131">使用者活動已起始中斷連線。</span><span class="sxs-lookup"><span data-stu-id="4632c-131">User activity has initiated the disconnect.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span><span class="sxs-lookup"><span data-stu-id="4632c-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-133">使用者登出，中斷會話的連線。</span><span class="sxs-lookup"><span data-stu-id="4632c-133">The user logged off, disconnecting the session.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span><span class="sxs-lookup"><span data-stu-id="4632c-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-135">內部授權錯誤。</span><span class="sxs-lookup"><span data-stu-id="4632c-135">Internal licensing error.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="4632c-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-137">沒有授權伺服器可用。</span><span class="sxs-lookup"><span data-stu-id="4632c-137">No license server was available.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span><span class="sxs-lookup"><span data-stu-id="4632c-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-139">未提供有效的軟體授權。</span><span class="sxs-lookup"><span data-stu-id="4632c-139">No valid software license was available.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span><span class="sxs-lookup"><span data-stu-id="4632c-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-141">遠端電腦收到不正確授權訊息。</span><span class="sxs-lookup"><span data-stu-id="4632c-141">The remote computer received a licensing message that was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span><span class="sxs-lookup"><span data-stu-id="4632c-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-143">硬體識別碼不符合軟體授權上指定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4632c-143">The hardware ID does not match the one designated on the software license.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span><span class="sxs-lookup"><span data-stu-id="4632c-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-145">用戶端授權錯誤。</span><span class="sxs-lookup"><span data-stu-id="4632c-145">Client license error.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span><span class="sxs-lookup"><span data-stu-id="4632c-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-147">授權通訊協定期間發生網路問題。</span><span class="sxs-lookup"><span data-stu-id="4632c-147">Network problems occurred during the licensing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span><span class="sxs-lookup"><span data-stu-id="4632c-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-149">用戶端已提前結束授權通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4632c-149">The client ended the licensing protocol prematurely.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span><span class="sxs-lookup"><span data-stu-id="4632c-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-151">授權訊息的加密錯誤。</span><span class="sxs-lookup"><span data-stu-id="4632c-151">A licensing message was encrypted incorrectly.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span><span class="sxs-lookup"><span data-stu-id="4632c-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-153">無法升級或更新本機電腦的用戶端存取授權。</span><span class="sxs-lookup"><span data-stu-id="4632c-153">The local computer's client access license could not be upgraded or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span><span class="sxs-lookup"><span data-stu-id="4632c-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-155">遠端電腦未獲得接受遠端連線的授權。</span><span class="sxs-lookup"><span data-stu-id="4632c-155">The remote computer is not licensed to accept remote connections.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span><span class="sxs-lookup"><span data-stu-id="4632c-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-157">建立授權存放的登錄機碼時，收到拒絕存取錯誤。</span><span class="sxs-lookup"><span data-stu-id="4632c-157">An access denied error was received while creating a registry key for the license store.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span><span class="sxs-lookup"><span data-stu-id="4632c-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-159">遇到不正確認證。</span><span class="sxs-lookup"><span data-stu-id="4632c-159">Invalid credentials were encountered.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span><span class="sxs-lookup"><span data-stu-id="4632c-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-161">開始內部通訊協定錯誤的範圍。</span><span class="sxs-lookup"><span data-stu-id="4632c-161">Beginning the range of internal protocol errors.</span></span> <span data-ttu-id="4632c-162">請檢查伺服器事件記錄檔以取得其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4632c-162">Check the server event log for additional details.</span></span>

</dd> <dt>

<span data-ttu-id="4632c-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span><span class="sxs-lookup"><span data-stu-id="4632c-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span></span>
</dt> <dd>

<span data-ttu-id="4632c-164">結束內部通訊協定錯誤的範圍。</span><span class="sxs-lookup"><span data-stu-id="4632c-164">Ending the range of internal protocol errors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4632c-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="4632c-165">Requirements</span></span>



| <span data-ttu-id="4632c-166">需求</span><span class="sxs-lookup"><span data-stu-id="4632c-166">Requirement</span></span> | <span data-ttu-id="4632c-167">值</span><span class="sxs-lookup"><span data-stu-id="4632c-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4632c-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4632c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="4632c-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4632c-169">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4632c-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4632c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="4632c-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4632c-171">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4632c-172">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4632c-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="4632c-173"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4632c-173"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4632c-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4632c-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4632c-175">**ExtendedDisconnectReason**</span><span class="sxs-lookup"><span data-stu-id="4632c-175">**ExtendedDisconnectReason**</span></span>](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





