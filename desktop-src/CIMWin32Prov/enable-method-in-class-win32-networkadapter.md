---
description: 啟用網路介面卡。
ms.assetid: ceb71e1b-5107-420f-a677-814307340469
ms.tgt_platform: multiple
title: Enable Win32_NetworkAdapter 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a7653d0bcda28ca333bc5c70bdcd69bce382787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187684"
---
# <a name="enable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="4d2fa-103">Enable Win32 \_ NetworkAdapter 類別的方法</span><span class="sxs-lookup"><span data-stu-id="4d2fa-103">Enable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="4d2fa-104">**Enable** 方法可啟用網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-104">The **Enable** method enables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d2fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d2fa-105">Syntax</span></span>


```mof
uint32 Enable();
```



## <a name="parameters"></a><span data-ttu-id="4d2fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d2fa-106">Parameters</span></span>

<span data-ttu-id="4d2fa-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d2fa-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d2fa-108">Return value</span></span>

<span data-ttu-id="4d2fa-109">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="4d2fa-110">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-110">Any other number indicates an error.</span></span> <span data-ttu-id="4d2fa-111">如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d2fa-112">備註</span><span class="sxs-lookup"><span data-stu-id="4d2fa-112">Remarks</span></span>

<span data-ttu-id="4d2fa-113">如果您的應用程式不是系統管理員存取權 privilidges，您可能會在使用此方法時遇到困難。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-113">You may experience difficulty using this method if your application does not administrator access privilidges.</span></span>

## <a name="examples"></a><span data-ttu-id="4d2fa-114">範例</span><span class="sxs-lookup"><span data-stu-id="4d2fa-114">Examples</span></span>

<span data-ttu-id="4d2fa-115">下列 Visual Basic 腳本範例會啟用第一個網路介面卡，並顯示 **NetEnabled** 屬性的狀態。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-115">The following Visual Basic Script example enables the first network adapter and shows the status of the **NetEnabled** property.</span></span> <span data-ttu-id="4d2fa-116">如需詳細資訊，請參閱 [**swbemobjectset 搭配使用. ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex)。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-116">For more information, see [**SWbemObjectSet.ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colAdapters = _
    objWMIService.Execquery_
        ("Select * from Win32_NetworkAdapter Where NetEnabled=False")
For Each Adapter in colAdapters
    WScript.Echo Adapter.DeviceId & "    " & Adapter.Name
Next
errReturn = colAdapters.ItemIndex(0).Enable()
If errReturn <> 0 Then
    WScript.Echo "Enable Network adapter failed for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId
Else 
    WScript.Echo "Enable Network adapter succeeded for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId 
End If 
WScript.Echo "NetEnabled= " & colAdapters.ItemIndex(0).NetEnabled
```



## <a name="requirements"></a><span data-ttu-id="4d2fa-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d2fa-117">Requirements</span></span>



| <span data-ttu-id="4d2fa-118">需求</span><span class="sxs-lookup"><span data-stu-id="4d2fa-118">Requirement</span></span> | <span data-ttu-id="4d2fa-119">值</span><span class="sxs-lookup"><span data-stu-id="4d2fa-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2fa-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d2fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4d2fa-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d2fa-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d2fa-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d2fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4d2fa-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d2fa-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d2fa-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d2fa-124">Namespace</span></span><br/>                | <span data-ttu-id="4d2fa-125">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4d2fa-125">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4d2fa-126">MOF</span><span class="sxs-lookup"><span data-stu-id="4d2fa-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d2fa-127"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d2fa-127"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d2fa-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4d2fa-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d2fa-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d2fa-129"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d2fa-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d2fa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d2fa-131">**Win32 \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="4d2fa-131">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="4d2fa-132">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="4d2fa-132">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="4d2fa-133">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="4d2fa-133">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

