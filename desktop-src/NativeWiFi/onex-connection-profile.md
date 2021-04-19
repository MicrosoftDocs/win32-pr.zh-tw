---
description: 包含目前用於 802.1 X 驗證之 802.1 X 連接設定檔的相關資訊。
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: ONEX_CONNECTION_PROFILE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974440"
---
# <a name="onex_connection_profile-structure"></a><span data-ttu-id="f6c90-103">ONEX \_ 連接 \_ 設定檔結構</span><span class="sxs-lookup"><span data-stu-id="f6c90-103">ONEX\_CONNECTION\_PROFILE structure</span></span>

<span data-ttu-id="f6c90-104">**ONEX 連線 \_ \_ 設定檔** 結構包含目前用於 802.1 X 驗證之 802.1 x 連線設定檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f6c90-104">The **ONEX\_CONNECTION\_PROFILE** structure contains information on the 802.1X connection profile currently used for 802.1X authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c90-105">語法</span><span class="sxs-lookup"><span data-stu-id="f6c90-105">Syntax</span></span>


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a><span data-ttu-id="f6c90-106">成員</span><span class="sxs-lookup"><span data-stu-id="f6c90-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6c90-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="f6c90-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-108">此 **ONEX \_ 連接 \_ 設定檔** 結構的版本。</span><span class="sxs-lookup"><span data-stu-id="f6c90-108">The version of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-109">**dwTotalLen**</span><span class="sxs-lookup"><span data-stu-id="f6c90-109">**dwTotalLen**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-110">此 **ONEX \_ 連接 \_ 設定檔** 結構的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6c90-110">The length, in bytes, of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-111">**fOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="f6c90-111">**fOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-112">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwOneXSupplicantFlags** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-112">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwOneXSupplicantFlags** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-113">**fsupplicantMode**</span><span class="sxs-lookup"><span data-stu-id="f6c90-113">**fsupplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-114">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **supplicantMode** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-114">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **supplicantMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-115">**fauthMode**</span><span class="sxs-lookup"><span data-stu-id="f6c90-115">**fauthMode**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-116">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **authMode** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-116">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **authMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-117">**fHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="f6c90-117">**fHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-118">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwHeldPeriod** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-118">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwHeldPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-119">**fAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="f6c90-119">**fAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-120">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwAuthPeriod** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-120">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwAuthPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-121">**fStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="f6c90-121">**fStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-122">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwStartPeriod** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-122">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwStartPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-123">**fMaxStart**</span><span class="sxs-lookup"><span data-stu-id="f6c90-123">**fMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-124">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwMaxStart** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-124">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxStart** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-125">**fMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="f6c90-125">**fMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-126">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwMaxAuthFailures** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-126">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxAuthFailures** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-127">**fNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="f6c90-127">**fNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-128">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwNetworkAuthTimeout** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-128">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthTimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-129">**fAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="f6c90-129">**fAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-130">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **bAllowLogonDialogs** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-130">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bAllowLogonDialogs** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-131">**fNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="f6c90-131">**fNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-132">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **dwNetworkAuthWithUITimeout** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-132">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthWithUITimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-133">**fUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="f6c90-133">**fUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-134">指出 **ONEX \_ 連接 \_ 設定檔** 結構是否包含 **bUserBasedVLan** 成員中的有效資料。</span><span class="sxs-lookup"><span data-stu-id="f6c90-134">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bUserBasedVLan** member.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-135">**dwOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="f6c90-135">**dwOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-136">可以存在於設定檔中的一組 802.1 X 旗標。</span><span class="sxs-lookup"><span data-stu-id="f6c90-136">A set of 802.1X flags that can be present in the profile.</span></span> <span data-ttu-id="f6c90-137">802.1 X 驗證模組會保留這些旗標供內部使用。</span><span class="sxs-lookup"><span data-stu-id="f6c90-137">These flags are reserved for internal use by the 802.1X authentication module.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-138">**supplicantMode**</span><span class="sxs-lookup"><span data-stu-id="f6c90-138">**supplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-139">802.1 X 架構中的 supplicantMode 元素，可指定用於 EAPOL-Start 訊息的傳輸方法。</span><span class="sxs-lookup"><span data-stu-id="f6c90-139">The supplicantMode element in the 802.1X schema that specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="f6c90-140">如需詳細資訊，請參閱 802.1 X 配置中的 [**supplicantMode (OneX) 元素**](onexschema-supplicantmode-onex-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6c90-140">For more information, see the [**supplicantMode (OneX) Element**](onexschema-supplicantmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="f6c90-141">值</span><span class="sxs-lookup"><span data-stu-id="f6c90-141">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="f6c90-142">意義</span><span class="sxs-lookup"><span data-stu-id="f6c90-142">Meaning</span></span>                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <span data-ttu-id="f6c90-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6c90-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f6c90-144">EAPOL-Start 不會傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="f6c90-144">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="f6c90-145">僅適用于有線局域網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="f6c90-145">Valid for wired LAN profiles only.</span></span><br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <span data-ttu-id="f6c90-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f6c90-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="f6c90-147">用戶端會根據網路功能決定傳送 EAPOL-Start 封包的時機。</span><span class="sxs-lookup"><span data-stu-id="f6c90-147">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="f6c90-148">EAPOL-Start 訊息只會在必要時傳送。</span><span class="sxs-lookup"><span data-stu-id="f6c90-148">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="f6c90-149">僅適用于有線局域網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="f6c90-149">Valid for wired LAN profiles only.</span></span><br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <span data-ttu-id="f6c90-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6c90-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="f6c90-151">EAPOL-Start 的訊息會由 802.1 X 所指定的方式傳輸。</span><span class="sxs-lookup"><span data-stu-id="f6c90-151">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="f6c90-152">適用于有線和無線局域網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="f6c90-152">Valid for both wired and wireless LAN profiles.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="f6c90-153">**authMode**</span><span class="sxs-lookup"><span data-stu-id="f6c90-153">**authMode**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-154">802.1 X 架構中的 authMode 元素，可指定用於 802.1 X 驗證的認證類型。</span><span class="sxs-lookup"><span data-stu-id="f6c90-154">The authMode element in the 802.1X schema that specifies the type of credentials used for 802.1X authentication.</span></span> <span data-ttu-id="f6c90-155">如需詳細資訊，請參閱 802.1 X 配置中的 [**authMode (OneX) 元素**](onexschema-authmode-onex-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6c90-155">For more information, see the [**authMode (OneX) Element**](onexschema-authmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="f6c90-156">值</span><span class="sxs-lookup"><span data-stu-id="f6c90-156">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="f6c90-157">意義</span><span class="sxs-lookup"><span data-stu-id="f6c90-157">Meaning</span></span>                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <span data-ttu-id="f6c90-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6c90-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f6c90-159">使用電腦或使用者認證。</span><span class="sxs-lookup"><span data-stu-id="f6c90-159">Use machine or user credentials.</span></span> <span data-ttu-id="f6c90-160">當使用者登入時，會使用使用者的認證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="f6c90-160">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="f6c90-161">當使用者未登入時，會使用電腦認證。</span><span class="sxs-lookup"><span data-stu-id="f6c90-161">When no user is logged on, machine credentials are used.</span></span><br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <span data-ttu-id="f6c90-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f6c90-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="f6c90-163">只使用電腦認證。</span><span class="sxs-lookup"><span data-stu-id="f6c90-163">Use machine credentials only.</span></span><br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <span data-ttu-id="f6c90-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6c90-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="f6c90-165">僅使用使用者認證。</span><span class="sxs-lookup"><span data-stu-id="f6c90-165">Use user credentials only.</span></span><br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <span data-ttu-id="f6c90-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f6c90-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span></span> </dl>                                 | <span data-ttu-id="f6c90-167">僅使用來賓 (空白) 認證。</span><span class="sxs-lookup"><span data-stu-id="f6c90-167">Use guest (empty) credentials only.</span></span><br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <span data-ttu-id="f6c90-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f6c90-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="f6c90-169">未指定要使用的認證。</span><span class="sxs-lookup"><span data-stu-id="f6c90-169">Credentials to use are not specified.</span></span><br/>                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="f6c90-170">**dwHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="f6c90-170">**dwHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-171">802.1 X 架構中的 heldPeriod 專案，指定用戶端在驗證嘗試失敗之後不會重新嘗試驗證的時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6c90-171">The heldPeriod element in the 802.1X schema that specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span> <span data-ttu-id="f6c90-172">如需詳細資訊，請參閱 802.1 X 配置中的 [**heldPeriod (OneX) 元素**](onexschema-heldperiod-onex-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6c90-172">For more information, see the [**heldPeriod (OneX) Element**](onexschema-heldperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-173">**dwAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="f6c90-173">**dwAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-174">802.1 X 架構中的 authPeriod 元素，可指定用戶端等候驗證器回應的時間長度上限（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6c90-174">The authPeriod element in the 802.1X schema that specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="f6c90-175">如果在指定的期間內未收到回應，用戶端會假設網路上沒有任何驗證器存在。</span><span class="sxs-lookup"><span data-stu-id="f6c90-175">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="f6c90-176">如需詳細資訊，請參閱 802.1 X 配置中的 [**authPeriod (OneX) 元素**](onexschema-authperiod-onex-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6c90-176">For more information, see the [**authPeriod (OneX) Element**](onexschema-authperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-177">**dwStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="f6c90-177">**dwStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-178">802.1 X 架構中的 startPeriod 元素，可指定傳送 EAPOL-Start 之前等候的時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6c90-178">The startPeriod element in the 802.1X schema that specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="f6c90-179">傳送 EAPOL-Start 訊息以啟動 802.1 X 驗證程式。</span><span class="sxs-lookup"><span data-stu-id="f6c90-179">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span> <span data-ttu-id="f6c90-180">如需詳細資訊，請參閱 802.1 X 配置中的 [**startPeriod (OneX) 元素**](onexschema-startperiod-onex-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6c90-180">For more information, see the [**startPeriod (OneX) Element**](onexschema-startperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-181">**dwMaxStart**</span><span class="sxs-lookup"><span data-stu-id="f6c90-181">**dwMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-182">802.1 X 架構中的 maxStart 元素，可指定傳送 EAPOL-Start 訊息的數目上限。</span><span class="sxs-lookup"><span data-stu-id="f6c90-182">The maxStart element in the 802.1X schema that specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="f6c90-183">在傳送 EAPOL-Start 訊息的數目上限之後，用戶端會假設網路上沒有任何驗證器存在。</span><span class="sxs-lookup"><span data-stu-id="f6c90-183">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="f6c90-184">如需詳細資訊，請參閱 802.1 X 配置中的 [**maxStart (OneX) 元素**](onexschema-maxstart-onex-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6c90-184">For more information, see the [**maxStart (OneX) Element**](onexschema-maxstart-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-185">**dwMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="f6c90-185">**dwMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-186">802.1 X 架構中的 maxAuthFailures 元素，可指定一組認證所允許的驗證失敗次數上限。</span><span class="sxs-lookup"><span data-stu-id="f6c90-186">The maxAuthFailures element in the 802.1X schema that specifies the maximum number of authentication failures allowed for a set of credentials.</span></span> <span data-ttu-id="f6c90-187">如需詳細資訊，請參閱 802.1 X 架構中的 [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="f6c90-187">For more information, see the [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-188">**dwNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="f6c90-188">**dwNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-189">在正常登入進行之前等候 802.1 X 驗證完成的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6c90-189">The time, in seconds, to wait for 802.1X authentication completion before normal logon proceeds.</span></span> <span data-ttu-id="f6c90-190">此值用於單一登入 (SSO) 案例。</span><span class="sxs-lookup"><span data-stu-id="f6c90-190">This value is used in single signon (SSO) scenarios.</span></span> <span data-ttu-id="f6c90-191">在 802.1 X 設定檔中，此值會預設為10秒。</span><span class="sxs-lookup"><span data-stu-id="f6c90-191">This value defaults to 10 seconds in an 802.1X profile.</span></span> <span data-ttu-id="f6c90-192">如需詳細資訊，請參閱 802.1 X 架構中的 [**maxDelay (singleSignOn) 元素**](onexschema-maxdelay-singlesignon-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6c90-192">For more information, see the [**maxDelay (singleSignOn) Element**](onexschema-maxdelay-singlesignon-element.md) in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-193">**dwNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="f6c90-193">**dwNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-194">如果使用者介面對話方塊需要使用者輸入，則在每個登入的 SSO 中顯示時，等候連接的最長持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6c90-194">The maximum duration time, in seconds, to wait for a connection in case a user interface dialog box that requires user input is displayed during the per-logon SSO.</span></span>

<span data-ttu-id="f6c90-195">在 Windows Vista SP1 和更新版本上，此值會硬式編碼為10分鐘，且無法設定。</span><span class="sxs-lookup"><span data-stu-id="f6c90-195">On Windows Vista with SP1 and later, this value is hardcoded to 10 minutes and is not configurable.</span></span> <span data-ttu-id="f6c90-196">在 Windows Vista 發行至製造業時，此值在 802.1 X 設定檔中的預設值為60秒，而且是由架構中的 **maxDelayWithAdditionalDialogs** 元素所控制。</span><span class="sxs-lookup"><span data-stu-id="f6c90-196">On Windows Vista Release to Manufacturing, this value defaults to 60 seconds in an 802.1X profile and was controlled by the **maxDelayWithAdditionalDialogs** element in the schema.</span></span>

<span data-ttu-id="f6c90-197">在 Windows Vista SP1 和更新版本中，會忽略並取代 802.1 X 架構中的 **maxDelayWithAdditionalDialogs** 元素。</span><span class="sxs-lookup"><span data-stu-id="f6c90-197">On Windows Vista with SP1 and later, the **maxDelayWithAdditionalDialogs** element in the 802.1X schema is ignored and deprecated.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-198">**bAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="f6c90-198">**bAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-199">值，指定是否允許在使用預先登錄 SSO 時顯示 EAP 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f6c90-199">A value that specifies whether to allow EAP dialogs to be displayed when using pre-logon SSO.</span></span> <span data-ttu-id="f6c90-200">如需詳細資訊，請參閱 802.1 X 架構中的 **allowAdditionalDialogs** 元素。</span><span class="sxs-lookup"><span data-stu-id="f6c90-200">For more information, see the **allowAdditionalDialogs** element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="f6c90-201">**bUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="f6c90-201">**bUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="f6c90-202">802.1 X 架構中的 userBasedVirtualLan 元素，可指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。</span><span class="sxs-lookup"><span data-stu-id="f6c90-202">The userBasedVirtualLan element in the 802.1X schema that specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="f6c90-203">有些網路存取伺服器 (NAS) 裝置會在使用者驗證之後變更 VLAN。</span><span class="sxs-lookup"><span data-stu-id="f6c90-203">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="f6c90-204">當 userBasedVirtualLan 為 TRUE 時，NAS 可能會在使用者驗證之後變更裝置的 VLAN。</span><span class="sxs-lookup"><span data-stu-id="f6c90-204">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span> <span data-ttu-id="f6c90-205">如需詳細資訊，請參閱 802.1 X 配置中的 [**userBasedVirtualLan (singleSignOn) 元素**](onexschema-userbasedvirtuallan-singlesignon-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6c90-205">For more information, see the [**userBasedVirtualLan (singleSignOn) Element**](onexschema-userbasedvirtuallan-singlesignon-element.md) in the 802.1X scheme.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6c90-206">備註</span><span class="sxs-lookup"><span data-stu-id="f6c90-206">Remarks</span></span>

<span data-ttu-id="f6c90-207">802.1 X 模組會使用 **ONEX 連線 \_ \_ 設定檔** 結構，這是 Windows Vista 和更新版本支援的新無線設定元件。</span><span class="sxs-lookup"><span data-stu-id="f6c90-207">The **ONEX\_CONNECTION\_PROFILE** structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and later.</span></span>

<span data-ttu-id="f6c90-208">[**ONEX \_ 結果 \_ 更新 \_ 資料**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)報含 802.1 x 驗證狀態變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="f6c90-208">The [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contains information on a status change to 802.1X authentication.</span></span> <span data-ttu-id="f6c90-209">當 [**wlan \_ 通知 \_ 資料**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))結構的 **NotificationSource** 成員是 **wlan \_ 通知 \_ 來源 \_ ONEX** ，且收到通知之 **wlan \_ 通知 \_ 資料** 結構的 **NotificationCode** 成員為 **OneXNotificationTypeResultUpdate** 時，會傳回 **ONEX \_ 結果 \_ 更新 \_ 資料** 結構。</span><span class="sxs-lookup"><span data-stu-id="f6c90-209">The **ONEX\_RESULT\_UPDATE\_DATA** structure is returned when the **NotificationSource** member of the [**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) structure is **WLAN\_NOTIFICATION\_SOURCE\_ONEX** and the **NotificationCode** member of the **WLAN\_NOTIFICATION\_DATA** structure for received notification is **OneXNotificationTypeResultUpdate**.</span></span> <span data-ttu-id="f6c90-210">針對此通知， **WLAN \_ 通知 \_ 資料** 結構的 **.pdata** 成員會指向包含 802.1 x 驗證狀態變更相關資訊的 **ONEX \_ 結果 \_ 更新 \_ 資料** 結構。</span><span class="sxs-lookup"><span data-stu-id="f6c90-210">For this notification, the **pData** member of the **WLAN\_NOTIFICATION\_DATA** structure points to an **ONEX\_RESULT\_UPDATE\_DATA** structure that contains information on the 802.1X authentication status change.</span></span>

<span data-ttu-id="f6c90-211">如果已設定 [**onex \_ 結果 \_ 更新 \_ 資料**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)結構中的 **fOneXAuthParams** 成員，則 **onex \_ 結果 \_ 更新 \_ 資料** 結構的 **AuthParams** 成員會包含一個 [**onex \_ 變數 \_ BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)結構，其中包含從 **onex \_ 變數 \_ blob** 的 **dwOffset** 成員開始內嵌的 [**onex \_ AUTH \_ PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)結構。</span><span class="sxs-lookup"><span data-stu-id="f6c90-211">If the **fOneXAuthParams** member in the [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) structure is set, then the **authParams** member of the **ONEX\_RESULT\_UPDATE\_DATA** structure contains an [**ONEX\_VARIABLE\_BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) structure with an [**ONEX\_AUTH\_PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span> <span data-ttu-id="f6c90-212">**Onex \_ AUTH \_ PARAMS** 結構的 **oneXConnProfile** 成員包含一個 **Onex \_ 變數 \_ BLOB** 結構，其中的 **Onex \_ 連接 \_ 設定檔** 結構是從 **onex \_ 變數 \_ blob** 的 **dwOffset** 成員開始。</span><span class="sxs-lookup"><span data-stu-id="f6c90-212">The **oneXConnProfile** member of the **ONEX\_AUTH\_PARAMS** structure contains an **ONEX\_VARIABLE\_BLOB** structure with an **ONEX\_CONNECTION\_PROFILE** structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span>

<span data-ttu-id="f6c90-213">在公用標頭檔中未定義 **ONEX \_ 連接 \_ 設定檔** 結構。</span><span class="sxs-lookup"><span data-stu-id="f6c90-213">The **ONEX\_CONNECTION\_PROFILE** structure is not defined in a public header file.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c90-214">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6c90-214">Requirements</span></span>



| <span data-ttu-id="f6c90-215">需求</span><span class="sxs-lookup"><span data-stu-id="f6c90-215">Requirement</span></span> | <span data-ttu-id="f6c90-216">值</span><span class="sxs-lookup"><span data-stu-id="f6c90-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f6c90-217">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6c90-217">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c90-218">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6c90-218">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f6c90-219">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6c90-219">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c90-220">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6c90-220">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6c90-221">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6c90-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6c90-222">關於當的架構</span><span class="sxs-lookup"><span data-stu-id="f6c90-222">About the ACM Architecture</span></span>](about-the-acm-architecture.md)
</dt> <dt>

[<span data-ttu-id="f6c90-223">OneX 架構</span><span class="sxs-lookup"><span data-stu-id="f6c90-223">OneX Schema</span></span>](onexschema-schema.md)
</dt> <dt>

[<span data-ttu-id="f6c90-224">**authMode (OneX) 元素**</span><span class="sxs-lookup"><span data-stu-id="f6c90-224">**authMode (OneX) Element**</span></span>](onexschema-authmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="f6c90-225">**authPeriod (OneX) 元素**</span><span class="sxs-lookup"><span data-stu-id="f6c90-225">**authPeriod (OneX) Element**</span></span>](onexschema-authperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="f6c90-226">**heldPeriod (OneX) 元素**</span><span class="sxs-lookup"><span data-stu-id="f6c90-226">**heldPeriod (OneX) Element**</span></span>](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="f6c90-227">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="f6c90-227">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[<span data-ttu-id="f6c90-228">**maxStart (OneX) 元素**</span><span class="sxs-lookup"><span data-stu-id="f6c90-228">**maxStart (OneX) Element**</span></span>](onexschema-maxstart-onex-element.md)
</dt> <dt>

[<span data-ttu-id="f6c90-229">**startPeriod (OneX) 元素**</span><span class="sxs-lookup"><span data-stu-id="f6c90-229">**startPeriod (OneX) Element**</span></span>](onexschema-startperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="f6c90-230">**supplicantMode (OneX) 元素**</span><span class="sxs-lookup"><span data-stu-id="f6c90-230">**supplicantMode (OneX) Element**</span></span>](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="f6c90-231">**userBasedVirtualLan (singleSignOn) 元素**</span><span class="sxs-lookup"><span data-stu-id="f6c90-231">**userBasedVirtualLan (singleSignOn) Element**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[<span data-ttu-id="f6c90-232">**ONEX \_ AUTH \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="f6c90-232">**ONEX\_AUTH\_PARAMS**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[<span data-ttu-id="f6c90-233">**ONEX \_ 通知 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f6c90-233">**ONEX\_NOTIFICATION\_TYPE**</span></span>](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[<span data-ttu-id="f6c90-234">**ONEX \_ 結果 \_ 更新 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="f6c90-234">**ONEX\_RESULT\_UPDATE\_DATA**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[<span data-ttu-id="f6c90-235">**OneX 架構元素**</span><span class="sxs-lookup"><span data-stu-id="f6c90-235">**OneX Schema Element**</span></span>](onexschema-onex-element.md)
</dt> <dt>

[<span data-ttu-id="f6c90-236">**ONEX \_ 變數 \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="f6c90-236">**ONEX\_VARIABLE\_BLOB**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

<span data-ttu-id="f6c90-237">[**WLAN \_ 通知 \_ 資料**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6c90-237">[**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f6c90-238">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="f6c90-238">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
