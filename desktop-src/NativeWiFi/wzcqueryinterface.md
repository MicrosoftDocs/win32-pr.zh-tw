---
description: 針對無線零設定服務所管理的無線區域網路介面，提供詳細的資訊。
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: 'WZCQueryInterface 函式 (Wzcsapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851787"
---
# <a name="wzcqueryinterface-function"></a><span data-ttu-id="5db4f-103">WZCQueryInterface 函式</span><span class="sxs-lookup"><span data-stu-id="5db4f-103">WZCQueryInterface function</span></span>

<span data-ttu-id="5db4f-104">\[Windows Vista 和 Windows Server 2008 已不再支援 **WZCQueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="5db4f-104">\[**WZCQueryInterface** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="5db4f-105">請改用 [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) 函數。</span><span class="sxs-lookup"><span data-stu-id="5db4f-105">Use the [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) function instead.</span></span> <span data-ttu-id="5db4f-106">如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。</span><span class="sxs-lookup"><span data-stu-id="5db4f-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).</span></span> <span data-ttu-id="5db4f-107">\]</span><span class="sxs-lookup"><span data-stu-id="5db4f-107">\]</span></span>

<span data-ttu-id="5db4f-108">**WZCQueryInterface** 函式會針對無線零設定服務所管理的無線區域網路介面，提供詳細的資訊。</span><span class="sxs-lookup"><span data-stu-id="5db4f-108">The **WZCQueryInterface** function provides detailed information for a wireless LAN interface managed by the Wireless Zero Configuration service.</span></span>

<span data-ttu-id="5db4f-109">提供指定介面的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5db4f-109">Provides detailed information for a given interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db4f-110">語法</span><span class="sxs-lookup"><span data-stu-id="5db4f-110">Syntax</span></span>


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5db4f-111">參數</span><span class="sxs-lookup"><span data-stu-id="5db4f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db4f-112">*pSrvAddr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5db4f-112">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db4f-113">字串的指標，其中包含要在其上執行此函式的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="5db4f-113">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="5db4f-114">如果此參數為 **Null**，則會在本機電腦上查詢無線零設定服務。</span><span class="sxs-lookup"><span data-stu-id="5db4f-114">If this parameter is **NULL**, then the Wireless Zero Configuration service is queried on the local computer.</span></span>

<span data-ttu-id="5db4f-115">如果指定的 *pSrvAddr* 參數是遠端電腦，則遠端電腦必須支援遠端 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="5db4f-115">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="5db4f-116">*dwInFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5db4f-116">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db4f-117">要查詢的欄位。</span><span class="sxs-lookup"><span data-stu-id="5db4f-117">The fields to be queried.</span></span> <span data-ttu-id="5db4f-118">這是位元遮罩，可包含下列旗標的任何組合。</span><span class="sxs-lookup"><span data-stu-id="5db4f-118">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="5db4f-119">值</span><span class="sxs-lookup"><span data-stu-id="5db4f-119">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="5db4f-120">意義</span><span class="sxs-lookup"><span data-stu-id="5db4f-120">Meaning</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <span data-ttu-id="5db4f-121"><dt>**INTF \_DYNFLAGS**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-121"><dt>**INTF\_DYNFLAGS**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="5db4f-122">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **dwDynFlags** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="5db4f-122">Return the value for the **dwDynFlags** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="5db4f-123"><dt>**INTF \_描述**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-123"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>                      | <span data-ttu-id="5db4f-124">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **wszDescr** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="5db4f-124">Return the value for the **wszDescr** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="5db4f-125"><dt>**INTF \_NDISMEDIA**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-125"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="5db4f-126">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中的 **ulMediaState**、 **ulMediaType** 和 **ulPhysicalMediaType** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="5db4f-126">Return the values for the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <span data-ttu-id="5db4f-127"><dt>**INTF \_PREFLIST**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-127"><dt>**INTF\_PREFLIST**</dt> <dt>0x00040000</dt></span></span> </dl>             | <span data-ttu-id="5db4f-128">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構之 **rdStSSIDList** 成員中的慣用網路清單。</span><span class="sxs-lookup"><span data-stu-id="5db4f-128">Return the preferred list of networks in the **rdStSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <span data-ttu-id="5db4f-129"><dt>**INTF \_功能**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-129"><dt>**INTF\_CAPABILITIES**</dt> <dt>0x00080000</dt></span></span> </dl> | <span data-ttu-id="5db4f-130">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中的 **dwCapabilities** 和 **rdNicCapabilities** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="5db4f-130">Return the values for the **dwCapabilities** and the **rdNicCapabilities** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <span data-ttu-id="5db4f-131"><dt>**INTF \_INFRAMODE**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-131"><dt>**INTF\_INFRAMODE**</dt> <dt>0x00200000</dt></span></span> </dl>          | <span data-ttu-id="5db4f-132">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **nInfraMode** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="5db4f-132">Return the value for the **nInfraMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="5db4f-133">**NInfraMode** 成員只有在某些介面內容狀態中才有效。</span><span class="sxs-lookup"><span data-stu-id="5db4f-133">The **nInfraMode** member is valid only in some interface context states.</span></span><br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <span data-ttu-id="5db4f-134"><dt>**INTF \_AUTHMODE**</dt> <dt>0x00400000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-134"><dt>**INTF\_AUTHMODE**</dt> <dt>0x00400000</dt></span></span> </dl>             | <span data-ttu-id="5db4f-135">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **nAuthMode** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="5db4f-135">Return the value for the **nAuthMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="5db4f-136">**NAuthMode** 成員只有在某些介面內容狀態中才有效。</span><span class="sxs-lookup"><span data-stu-id="5db4f-136">The **nAuthMode** member is valid only in some interface context states.</span></span><br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <span data-ttu-id="5db4f-137"><dt>**INTF \_WEPSTATUS**</dt> <dt>0x00800000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-137"><dt>**INTF\_WEPSTATUS**</dt> <dt>0x00800000</dt></span></span> </dl>          | <span data-ttu-id="5db4f-138">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **nWepStatus** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="5db4f-138">Return the value for the **nWepStatus** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="5db4f-139">**NWepStatus** 成員只有在某些介面內容狀態中才有效。</span><span class="sxs-lookup"><span data-stu-id="5db4f-139">The **nWepStatus** member is valid only in some interface context states.</span></span><br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <span data-ttu-id="5db4f-140"><dt>**INTF \_SSID**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-140"><dt>**INTF\_SSID**</dt> <dt>0x01000000</dt></span></span> </dl>                         | <span data-ttu-id="5db4f-141">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **rdSSID** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="5db4f-141">Return the value for the **rdSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="5db4f-142">**RdSSID** 成員只有在某些介面內容狀態中才有效。</span><span class="sxs-lookup"><span data-stu-id="5db4f-142">The **rdSSID** member is valid only in some interface context states.</span></span><br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <span data-ttu-id="5db4f-143"><dt>**INTF \_BSSID**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-143"><dt>**INTF\_BSSID**</dt> <dt>0x02000000</dt></span></span> </dl>                      | <span data-ttu-id="5db4f-144">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **rdBSSID** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="5db4f-144">Return the value for the **rdBSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="5db4f-145">**RdBSSID** 成員只有在某些介面內容狀態中才有效。</span><span class="sxs-lookup"><span data-stu-id="5db4f-145">The **rdBSSID** member is valid only in some interface context states.</span></span><br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <span data-ttu-id="5db4f-146"><dt>**INTF \_BSSIDLIST**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-146"><dt>**INTF\_BSSIDLIST**</dt> <dt>0x04000000</dt></span></span> </dl>          | <span data-ttu-id="5db4f-147">傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構之 **rdBSSIDList** 成員中的網路可見清單。</span><span class="sxs-lookup"><span data-stu-id="5db4f-147">Return the visible list of networks in the **rdBSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="5db4f-148">**RdBSSIDList** 成員只有在某些介面內容狀態中才有效。</span><span class="sxs-lookup"><span data-stu-id="5db4f-148">The **rdBSSIDList** member is valid only in some interface context states.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5db4f-149">*pIntf* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5db4f-149">*pIntf* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5db4f-150">在輸入時，指向要查詢之介面索引鍵的指標。</span><span class="sxs-lookup"><span data-stu-id="5db4f-150">On input, a pointer to the key of the interface to query.</span></span> <span data-ttu-id="5db4f-151">在輸出時，為所要求介面資料的指標。</span><span class="sxs-lookup"><span data-stu-id="5db4f-151">On output, a pointer to the requested interface data.</span></span> <span data-ttu-id="5db4f-152">此參數是 [**INTF \_ 專案**](intf-entry.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5db4f-152">This parameter is a pointer to an [**INTF\_ENTRY**](intf-entry.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5db4f-153">*pdwOutFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5db4f-153">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5db4f-154">已成功抓取一組欄位。</span><span class="sxs-lookup"><span data-stu-id="5db4f-154">A set of fields successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db4f-155">傳回值</span><span class="sxs-lookup"><span data-stu-id="5db4f-155">Return value</span></span>

<span data-ttu-id="5db4f-156">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="5db4f-156">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5db4f-157">如果函式失敗，則傳回值可能是下列其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="5db4f-157">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="5db4f-158">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5db4f-158">Return code</span></span>                                                                                               | <span data-ttu-id="5db4f-159">Description</span><span class="sxs-lookup"><span data-stu-id="5db4f-159">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5db4f-160"><dt>**錯誤 \_ 領域 \_ 垃圾桶**</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-160"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="5db4f-161">儲存體控制區塊已損毀。</span><span class="sxs-lookup"><span data-stu-id="5db4f-161">The storage control blocks were destroyed.</span></span> <span data-ttu-id="5db4f-162">如果無線零設定服務尚未初始化內建物件，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5db4f-162">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="5db4f-163"><dt>**\_ \_ \_ 找不到錯誤檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-163"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="5db4f-164">系統找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="5db4f-164">The system cannot find the file specified.</span></span> <span data-ttu-id="5db4f-165">如果 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszGuid** 成員中的 GUID 與本機電腦上的任何無線區域網路介面不相符，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5db4f-165">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="5db4f-166"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-166"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="5db4f-167">參數不正確。</span><span class="sxs-lookup"><span data-stu-id="5db4f-167">A parameter is incorrect.</span></span> <span data-ttu-id="5db4f-168">如果 *pIntf* 參數為 **Null**，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5db4f-168">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="5db4f-169">如果 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszGuid** 成員為 **Null**，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5db4f-169">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="5db4f-170"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-170"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="5db4f-171">沒有足夠的記憶體可用來處理此要求，並配置記憶體給查詢結果。</span><span class="sxs-lookup"><span data-stu-id="5db4f-171">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="5db4f-172"><dt>**RPC \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-172"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="5db4f-173">不同的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5db4f-173">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="5db4f-174">備註</span><span class="sxs-lookup"><span data-stu-id="5db4f-174">Remarks</span></span>

<span data-ttu-id="5db4f-175">*PIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **WSZGUID** 成員，必須包含無線區域網路介面的介面 GUID。</span><span class="sxs-lookup"><span data-stu-id="5db4f-175">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="5db4f-176">您可以藉由呼叫 [**WZCEnumInterfaces**](wzcenuminterfaces.md) 函式來取出無線區域網路介面清單。</span><span class="sxs-lookup"><span data-stu-id="5db4f-176">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

<span data-ttu-id="5db4f-177">*PIntf* 所指向之 [**INTF \_ 專案**](intf-entry.md)結構的下列成員在呼叫 **WZCQueryInterface** 函式之前，必須先設定為0： **RdSSID**、 **rdBSSID**、 **rdBSSIDList**、 **rdStSSIDList** 和 **rdCtrlData**。</span><span class="sxs-lookup"><span data-stu-id="5db4f-177">The following members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* must be set to 0 before a call to the **WZCQueryInterface** function: **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData**.</span></span>

<span data-ttu-id="5db4f-178">即使收到媒體連線和中斷線上活動，無線零設定服務也不會 automotically 更新媒體狀態。</span><span class="sxs-lookup"><span data-stu-id="5db4f-178">The Wireless Zero Configuration service does not automotically update media state, even when media connected and disconnected events are received.</span></span> <span data-ttu-id="5db4f-179">應用程式應該在呼叫 WZCRefreshInterface 函式之前，藉由呼叫 [](wzcrefreshinterface.md)函式來強制執行媒體狀態重新 **整理，如果** 要要求 NDIS 媒體狀態 (\_ 會在 *dwInFlags* 參數) 中設定 INTF NDISMEDIA 位。</span><span class="sxs-lookup"><span data-stu-id="5db4f-179">An application should force a media state refresh by calling the [**WZCRefreshInterface**](wzcrefreshinterface.md) function before calling the **WZCQueryInterface** function if the NDIS media state is to be requested (the INTF\_NDISMEDIA bit will be set in the *dwInFlags* parameter).</span></span>

<span data-ttu-id="5db4f-180">當 *dwInFlags* 參數包含 **INTF \_ BSSIDLIST** 時，如果可見的網路清單是空的，則 **WZCQueryInterface** 函數不會將 *dwOutFlags* 設定為 INTF **\_ BSSIDLIST** 。</span><span class="sxs-lookup"><span data-stu-id="5db4f-180">When the *dwInFlags* parameter contains **INTF\_BSSIDLIST**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_BSSIDLIST** if the visible list of networks is empty.</span></span> <span data-ttu-id="5db4f-181">當 *dwInFlags* 參數包含 **INTF \_ ssid** 時，如果沒有可用的 ssid， **WZCQueryInterface** 函式不會設定 *dwOutFlags* 與 **INTF \_ ssid** 。</span><span class="sxs-lookup"><span data-stu-id="5db4f-181">When the *dwInFlags* parameter contains **INTF\_SSID**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_SSID** if no SSID is available.</span></span>

<span data-ttu-id="5db4f-182">如果 **WZCQueryInterface** 函式傳回錯誤 \_ 成功，呼叫端應該使用 *PIntf* 參數來呼叫 [**>localfree**](/windows/win32/api/winbase/nf-winbase-localfree)函式，以釋放配置給所傳回資料的內部緩衝區（一旦不再需要這項資訊）。</span><span class="sxs-lookup"><span data-stu-id="5db4f-182">If the **WZCQueryInterface** function returns ERROR\_SUCCESS, the caller should call the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function with the *pIntf* parameter to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span> <span data-ttu-id="5db4f-183">這會釋放 *rdCtrlData* 參數所指向 [**INTF \_ 專案**](intf-entry.md)結構的 **rdSSID**、 **rdBSSID**、 **rdBSSIDList**、 **rdStSSIDList** 和 **pIntf** 成員所使用的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5db4f-183">This releases the buffers used by the **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="5db4f-184">Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔和 *Wzcsapi .lib* 匯入程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="5db4f-184">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5db4f-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="5db4f-185">Requirements</span></span>



| <span data-ttu-id="5db4f-186">需求</span><span class="sxs-lookup"><span data-stu-id="5db4f-186">Requirement</span></span> | <span data-ttu-id="5db4f-187">值</span><span class="sxs-lookup"><span data-stu-id="5db4f-187">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5db4f-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5db4f-188">Minimum supported client</span></span><br/> | <span data-ttu-id="5db4f-189">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5db4f-189">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5db4f-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5db4f-190">Minimum supported server</span></span><br/> | <span data-ttu-id="5db4f-191">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5db4f-191">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5db4f-192">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5db4f-192">End of client support</span></span><br/>    | <span data-ttu-id="5db4f-193">Windows XP （含 SP3）</span><span class="sxs-lookup"><span data-stu-id="5db4f-193">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="5db4f-194">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5db4f-194">End of server support</span></span><br/>    | <span data-ttu-id="5db4f-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5db4f-195">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="5db4f-196">標頭</span><span class="sxs-lookup"><span data-stu-id="5db4f-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="5db4f-197"><dt>Wzcsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-197"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="5db4f-198">程式庫</span><span class="sxs-lookup"><span data-stu-id="5db4f-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="5db4f-199"><dt>Wzcsapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-199"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5db4f-200">DLL</span><span class="sxs-lookup"><span data-stu-id="5db4f-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5db4f-201"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5db4f-201"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5db4f-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5db4f-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db4f-203">**INTF \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="5db4f-203">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> <dt>

[<span data-ttu-id="5db4f-204">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="5db4f-204">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="5db4f-205">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="5db4f-205">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="5db4f-206">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="5db4f-206">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
