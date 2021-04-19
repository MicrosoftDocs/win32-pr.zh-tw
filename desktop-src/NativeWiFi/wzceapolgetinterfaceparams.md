---
description: 取得指定無線區域網路介面的 EAPOL 設定參數。
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: 'WZCEapolGetInterfaceParams 函式 (Wzcsapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994481"
---
# <a name="wzceapolgetinterfaceparams-function"></a><span data-ttu-id="0401e-103">WZCEapolGetInterfaceParams 函式</span><span class="sxs-lookup"><span data-stu-id="0401e-103">WZCEapolGetInterfaceParams function</span></span>

<span data-ttu-id="0401e-104">\[Windows Vista 和 Windows Server 2008 已不再支援 **WZCEapolGetInterfaceParams** 。</span><span class="sxs-lookup"><span data-stu-id="0401e-104">\[**WZCEapolGetInterfaceParams** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="0401e-105">相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。</span><span class="sxs-lookup"><span data-stu-id="0401e-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="0401e-106">如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]</span><span class="sxs-lookup"><span data-stu-id="0401e-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="0401e-107">**WZCEapolGetInterfaceParams** 函式會取得指定無線區域網路介面的 EAPOL 設定參數。</span><span class="sxs-lookup"><span data-stu-id="0401e-107">The **WZCEapolGetInterfaceParams** function gets EAPOL configuration parameters for the specified wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0401e-108">語法</span><span class="sxs-lookup"><span data-stu-id="0401e-108">Syntax</span></span>


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a><span data-ttu-id="0401e-109">參數</span><span class="sxs-lookup"><span data-stu-id="0401e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0401e-110">*pSrvAddr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0401e-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0401e-111">字串的指標，其中包含要在其上執行此函式的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="0401e-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="0401e-112">如果此參數為 **Null**，則會在本機電腦上呼叫無線零設定服務。</span><span class="sxs-lookup"><span data-stu-id="0401e-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="0401e-113">如果指定的 *pSrvAddr* 參數是遠端電腦，則遠端電腦必須支援遠端 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0401e-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="0401e-114">*pwszGuid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0401e-114">*pwszGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0401e-115">要抓取資料之介面的 GUID。</span><span class="sxs-lookup"><span data-stu-id="0401e-115">The GUID of the interface for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="0401e-116">*dwSizeOfSSID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0401e-116">*dwSizeOfSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0401e-117">要取出資料的網路識別碼大小。</span><span class="sxs-lookup"><span data-stu-id="0401e-117">The size of the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="0401e-118">*pbSSID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0401e-118">*pbSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0401e-119">要抓取其資料的網路識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="0401e-119">A pointer to the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="0401e-120">*pIntfParams* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0401e-120">*pIntfParams* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0401e-121">包含介面參數的 [**EAPOL \_ INTF \_ PARAMS 參數**](eapol-intf-params.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="0401e-121">A pointer to a [**EAPOL\_INTF\_PARAMS**](eapol-intf-params.md) structure that contains interface parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0401e-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="0401e-122">Return value</span></span>

<span data-ttu-id="0401e-123">如果作業 \_ 順利完成，則傳回錯誤成功; 否則會傳回其中一個 Windows 系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0401e-123">Returns ERROR\_SUCCESS if the operation completes successfully; otherwise, returns one of the Windows system error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="0401e-124">備註</span><span class="sxs-lookup"><span data-stu-id="0401e-124">Remarks</span></span>

<span data-ttu-id="0401e-125">如果 **WZCEapolGetInterfaceParams** 傳回錯誤 \_ 成功，呼叫端應該呼叫 [**>localfree**](/windows/win32/api/winbase/nf-winbase-localfree) 來釋出針對所傳回之資料所配置的內部緩衝區，而不再需要這項資訊。</span><span class="sxs-lookup"><span data-stu-id="0401e-125">If the **WZCEapolGetInterfaceParams** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="0401e-126">Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔和 *Wzcsapi .lib* 匯入程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="0401e-126">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0401e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0401e-127">Requirements</span></span>



| <span data-ttu-id="0401e-128">需求</span><span class="sxs-lookup"><span data-stu-id="0401e-128">Requirement</span></span> | <span data-ttu-id="0401e-129">值</span><span class="sxs-lookup"><span data-stu-id="0401e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0401e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0401e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0401e-131">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0401e-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0401e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0401e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0401e-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0401e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0401e-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0401e-134">End of client support</span></span><br/>    | <span data-ttu-id="0401e-135">Windows XP （含 SP3）</span><span class="sxs-lookup"><span data-stu-id="0401e-135">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="0401e-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="0401e-136">End of server support</span></span><br/>    | <span data-ttu-id="0401e-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0401e-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="0401e-138">標頭</span><span class="sxs-lookup"><span data-stu-id="0401e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0401e-139"><dt>Wzcsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="0401e-139"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="0401e-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="0401e-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="0401e-141"><dt>Wzcsapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0401e-141"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0401e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0401e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0401e-143"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0401e-143"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0401e-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0401e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0401e-145">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="0401e-145">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="0401e-146">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="0401e-146">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="0401e-147">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="0401e-147">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
