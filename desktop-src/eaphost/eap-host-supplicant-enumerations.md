---
title: EAPHost 要求者列舉
description: 瞭解 EAPHost 要求者 API 列舉，例如 EapHostPeerMethodResultReason 和隔離 \_ 狀態。
ms.assetid: ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e214682a9b94c98db5981a0df8c2b8619814f1e5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842715"
---
# <a name="eaphost-supplicant-enumerations"></a><span data-ttu-id="e2e2b-103">EAPHost 要求者列舉</span><span class="sxs-lookup"><span data-stu-id="e2e2b-103">EAPHost Supplicant Enumerations</span></span>

<span data-ttu-id="e2e2b-104">EAPHost 要求者 API 列舉如下所示。</span><span class="sxs-lookup"><span data-stu-id="e2e2b-104">The EAPHost Supplicant API enumerations are as follows.</span></span>



| <span data-ttu-id="e2e2b-105">列舉型別</span><span class="sxs-lookup"><span data-stu-id="e2e2b-105">Enumeration</span></span>                                                                  | <span data-ttu-id="e2e2b-106">描述</span><span class="sxs-lookup"><span data-stu-id="e2e2b-106">Description</span></span>                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2e2b-107">**EAP \_ 互動式 \_ UI \_ 資料 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e2e2b-107">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)     | <span data-ttu-id="e2e2b-108">指定提供給特定要求者 API 呼叫的互動式使用者介面內容資料類型集合。</span><span class="sxs-lookup"><span data-stu-id="e2e2b-108">Specifies the set of types of interactive user interface context data supplied to certain supplicant API calls.</span></span>    |
| [<span data-ttu-id="e2e2b-109">**EAP \_ 方法 \_ 屬性 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e2e2b-109">**EAP\_METHOD\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_type)              | <span data-ttu-id="e2e2b-110">Windows 7 或更新版本：指定方法屬性類型。</span><span class="sxs-lookup"><span data-stu-id="e2e2b-110">Windows 7 or later: Specifies the method property type.</span></span>                                                            |
| [<span data-ttu-id="e2e2b-111">**EAP \_ 方法 \_ 屬性 \_ 值 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e2e2b-111">**EAP\_METHOD\_PROPERTY\_VALUE\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_value_type) | <span data-ttu-id="e2e2b-112">Windows 7 或更新版本：指定方法屬性值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e2e2b-112">Windows 7 or later: Specifies the data type of a method property value.</span></span>                                            |
| [<span data-ttu-id="e2e2b-113">**EAPHOST \_ AUTH \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="e2e2b-113">**EAPHOST\_AUTH\_STATUS**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphost_auth_status)                         | <span data-ttu-id="e2e2b-114">定義一組可能的 EAP 驗證會話狀態值。</span><span class="sxs-lookup"><span data-stu-id="e2e2b-114">Defines the set of possible EAP authentication session status values.</span></span>                                              |
| [<span data-ttu-id="e2e2b-115">**EapHostPeerAuthParams**</span><span class="sxs-lookup"><span data-stu-id="e2e2b-115">**EapHostPeerAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)                       | <span data-ttu-id="e2e2b-116">定義可能的驗證參數值集。</span><span class="sxs-lookup"><span data-stu-id="e2e2b-116">Defines the set of possible authentication parameter values.</span></span>                                                       |
| [<span data-ttu-id="e2e2b-117">**EapHostPeerMethodResultReason**</span><span class="sxs-lookup"><span data-stu-id="e2e2b-117">**EapHostPeerMethodResultReason**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason)       | <span data-ttu-id="e2e2b-118">定義一組可能的原因，描述 EAP 方法傳回給要求者的結果。</span><span class="sxs-lookup"><span data-stu-id="e2e2b-118">Defines the set of possible reasons that describe the results returned by an EAP method to a supplicant.</span></span>           |
| [<span data-ttu-id="e2e2b-119">**EapHostPeerResponseAction**</span><span class="sxs-lookup"><span data-stu-id="e2e2b-119">**EapHostPeerResponseAction**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)               | <span data-ttu-id="e2e2b-120">定義 EAP 驗證器或對等方法可在驗證期間向要求者指出的一組動作。</span><span class="sxs-lookup"><span data-stu-id="e2e2b-120">Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.</span></span> |
| [<span data-ttu-id="e2e2b-121">**隔離 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="e2e2b-121">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)                                  | <span data-ttu-id="e2e2b-122">定義電腦的一組可能的隔離狀態值。</span><span class="sxs-lookup"><span data-stu-id="e2e2b-122">Defines the set of possible isolation status values of a machine.</span></span>                                                  |



 

 

 




