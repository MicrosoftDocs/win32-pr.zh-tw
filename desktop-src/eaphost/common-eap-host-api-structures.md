---
title: 常見的 EAPHost API 結構
description: 瞭解一般 EAPHost API 結構。 查看所有 EAPHost 技術所使用的結構清單。
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b44a94aae1f18336dae8c11a1dc0217dc7c8d08
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683129"
---
# <a name="common-eaphost-api-structures"></a><span data-ttu-id="a960b-104">常見的 EAPHost API 結構</span><span class="sxs-lookup"><span data-stu-id="a960b-104">Common EAPHost API Structures</span></span>

<span data-ttu-id="a960b-105">下表列出所有 EAPHost API 技術通用的結構。</span><span class="sxs-lookup"><span data-stu-id="a960b-105">The following table lists structures that are common to all EAPHost API technologies.</span></span>



| <span data-ttu-id="a960b-106">結構</span><span class="sxs-lookup"><span data-stu-id="a960b-106">Structure</span></span>                                                                | <span data-ttu-id="a960b-107">Description</span><span class="sxs-lookup"><span data-stu-id="a960b-107">Description</span></span>                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a960b-108">**EAP \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="a960b-108">**EAP\_ATTRIBUTE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | <span data-ttu-id="a960b-109">包含 EAP 屬性。</span><span class="sxs-lookup"><span data-stu-id="a960b-109">Contains an EAP attribute.</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="a960b-110">**EAP \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="a960b-110">**EAP\_ATTRIBUTES**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | <span data-ttu-id="a960b-111">包含 EAP 屬性的陣列。</span><span class="sxs-lookup"><span data-stu-id="a960b-111">Contains an array of EAP attributes.</span></span>                                                                                                                                                                                    |
| [<span data-ttu-id="a960b-112">**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 陣列**</span><span class="sxs-lookup"><span data-stu-id="a960b-112">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | <span data-ttu-id="a960b-113">包含一組 [**EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) 結構，其中共同包含從 EAP 單一登入 (SSO) 設定對話方塊取得的使用者輸入欄位資料。</span><span class="sxs-lookup"><span data-stu-id="a960b-113">Contains a set of [**EAP\_CONFIG\_INPUT\_FIELD\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) structures that collectively contain the user input field data obtained from an EAP Single-Sign-On (SSO) configuration dialog.</span></span> |
| [<span data-ttu-id="a960b-114">**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="a960b-114">**EAP\_CONFIG\_INPUT\_FIELD\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | <span data-ttu-id="a960b-115">包含與 EAP 單一登入 (SSO) 設定] 對話方塊中單一輸入欄位相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="a960b-115">Contains the data associated with a single input field on a EAP Single-Sign-On (SSO) configuration dialog.</span></span>                                                                                                              |
| [<span data-ttu-id="a960b-116">**EAP \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="a960b-116">**EAP\_ERROR**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | <span data-ttu-id="a960b-117">包含在 EAPHost 作業期間發生之錯誤的相關資料。</span><span class="sxs-lookup"><span data-stu-id="a960b-117">Contains data about an error that occurred during an EAPHost operation.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="a960b-118">**EAP \_ 方法 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="a960b-118">**EAP\_METHOD\_INFO**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | <span data-ttu-id="a960b-119">包含 EAP 方法的特定資料。</span><span class="sxs-lookup"><span data-stu-id="a960b-119">Contains specific data for an EAP method.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="a960b-120">**EAP \_ 方法 \_ 資訊， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="a960b-120">**EAP\_METHOD\_INFO\_EX**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | <span data-ttu-id="a960b-121">Windows Vista Service Pack 1 (SP1) 或更新版本：包含 EAP 方法的特定資料。</span><span class="sxs-lookup"><span data-stu-id="a960b-121">Windows Vista with Service Pack 1 (SP1) or later: Contains specific data for an EAP method.</span></span>                                                                                                                             |
| [<span data-ttu-id="a960b-122">**EAP \_ 方法 \_ 資訊 \_ 陣列**</span><span class="sxs-lookup"><span data-stu-id="a960b-122">**EAP\_METHOD\_INFO\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | <span data-ttu-id="a960b-123">包含用戶端電腦上所安裝之 EAP 方法的資訊。</span><span class="sxs-lookup"><span data-stu-id="a960b-123">Contains information on EAP methods installed on the client computer.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="a960b-124">**EAP \_ 方法 \_ 資訊 \_ 陣列 \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="a960b-124">**EAP\_METHOD\_INFO\_ARRAY\_EX**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | <span data-ttu-id="a960b-125">Windows Vista SP1 或更新版本：包含用戶端電腦上安裝的所有 EAP 方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a960b-125">Windows Vista with SP1 or later: Contains information about all of the EAP methods installed on the client computer.</span></span>                                                                                                    |
| [<span data-ttu-id="a960b-126">**EAP \_ 方法 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="a960b-126">**EAP\_METHOD\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | <span data-ttu-id="a960b-127">包含 EAP 方法的類型、識別和撰寫資料。</span><span class="sxs-lookup"><span data-stu-id="a960b-127">Contains type, identification, and author data for an EAP method.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="a960b-128">**EAP \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="a960b-128">**EAP\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | <span data-ttu-id="a960b-129">包含 EAP 方法的型別和廠商識別資料。</span><span class="sxs-lookup"><span data-stu-id="a960b-129">Contains type and vendor identification data for an EAP method.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="a960b-130">**EapPacket**</span><span class="sxs-lookup"><span data-stu-id="a960b-130">**EapPacket**</span></span>](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | <span data-ttu-id="a960b-131">包含在 EAP 驗證會話期間傳送之不透明資料的封包。</span><span class="sxs-lookup"><span data-stu-id="a960b-131">Contains a packet of opaque data sent during an EAP authentication session.</span></span>                                                                                                                                             |



 

 

 




