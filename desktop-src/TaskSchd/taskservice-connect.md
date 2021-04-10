---
title: TaskService 方法
description: 針對腳本，連接至遠端電腦，並將此介面上的所有後續呼叫與遠端會話產生關聯。
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Connect 方法工作排程器
- Connect 方法工作排程器，TaskService 物件
- TaskService 物件工作排程器，Connect 方法
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934139"
---
# <a name="taskserviceconnect-method"></a><span data-ttu-id="88b46-106">TaskService 方法</span><span class="sxs-lookup"><span data-stu-id="88b46-106">TaskService.Connect method</span></span>

<span data-ttu-id="88b46-107">針對腳本，連接至遠端電腦，並將此介面上的所有後續呼叫與遠端會話產生關聯。</span><span class="sxs-lookup"><span data-stu-id="88b46-107">For scripting, connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span> <span data-ttu-id="88b46-108">如果 serverName 參數是空的，則這個方法會在本機電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="88b46-108">If the serverName parameter is empty, then this method will execute on the local computer.</span></span> <span data-ttu-id="88b46-109">如果未指定 userId，則會使用目前的權杖。</span><span class="sxs-lookup"><span data-stu-id="88b46-109">If the userId is not specified, then the current token is used.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b46-110">語法</span><span class="sxs-lookup"><span data-stu-id="88b46-110">Syntax</span></span>


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="88b46-111">參數</span><span class="sxs-lookup"><span data-stu-id="88b46-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b46-112">*serverName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="88b46-112">*serverName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88b46-113">您要連接的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="88b46-113">The name of the computer that you want to connect to.</span></span> <span data-ttu-id="88b46-114">如果 serverName 參數是空的，則這個方法會在本機電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="88b46-114">If the serverName parameter is empty, then this method will execute on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="88b46-115">*使用者* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="88b46-115">*user* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88b46-116">連接到電腦時使用的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="88b46-116">The user name that is used during the connection to the computer.</span></span> <span data-ttu-id="88b46-117">如果未指定使用者，則會使用目前的權杖。</span><span class="sxs-lookup"><span data-stu-id="88b46-117">If the user is not specified, then the current token is used.</span></span>

</dd> <dt>

<span data-ttu-id="88b46-118">*網域* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="88b46-118">*domain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88b46-119">*使用者* 參數中所指定之使用者的網域。</span><span class="sxs-lookup"><span data-stu-id="88b46-119">The domain of the user specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="88b46-120">*密碼* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="88b46-120">*password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88b46-121">用來連接到電腦的密碼。</span><span class="sxs-lookup"><span data-stu-id="88b46-121">The password that is used to connect to the computer.</span></span> <span data-ttu-id="88b46-122">如果未指定使用者名稱和密碼，則會使用目前的權杖。</span><span class="sxs-lookup"><span data-stu-id="88b46-122">If the user name and password are not specified, then the current token is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b46-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="88b46-123">Return value</span></span>

<span data-ttu-id="88b46-124">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="88b46-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88b46-125">備註</span><span class="sxs-lookup"><span data-stu-id="88b46-125">Remarks</span></span>

<span data-ttu-id="88b46-126">在呼叫任何其他 [**TaskService**](taskservice.md)方法之前，應該先呼叫 **TaskService** 方法。</span><span class="sxs-lookup"><span data-stu-id="88b46-126">The **TaskService.Connect** method should be called before calling any of the other [**TaskService**](taskservice.md) methods.</span></span>

<span data-ttu-id="88b46-127">如果 Connect 方法失敗，您可以收集錯誤識別碼以找出錯誤的意義。</span><span class="sxs-lookup"><span data-stu-id="88b46-127">If the Connect method fails, you can collect the error identifier to find the meaning of the error.</span></span> <span data-ttu-id="88b46-128">下表列出錯誤識別碼及其描述。</span><span class="sxs-lookup"><span data-stu-id="88b46-128">The following table lists the error identifiers and their descriptions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88b46-129">錯誤識別碼</span><span class="sxs-lookup"><span data-stu-id="88b46-129">Error Identifier</span></span></th>
<th><span data-ttu-id="88b46-130">Description</span><span class="sxs-lookup"><span data-stu-id="88b46-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88b46-131">0x80070005</span><span class="sxs-lookup"><span data-stu-id="88b46-131">0x80070005</span></span></td>
<td><span data-ttu-id="88b46-132">拒絕存取以連接到工作排程器服務。</span><span class="sxs-lookup"><span data-stu-id="88b46-132">Access is denied to connect to the Task Scheduler service.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88b46-133">0x80041315</span><span class="sxs-lookup"><span data-stu-id="88b46-133">0x80041315</span></span></td>
<td><span data-ttu-id="88b46-134">工作排程器服務未執行。</span><span class="sxs-lookup"><span data-stu-id="88b46-134">The Task Scheduler service is not running.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88b46-135">0x8007000e</span><span class="sxs-lookup"><span data-stu-id="88b46-135">0x8007000e</span></span></td>
<td><span data-ttu-id="88b46-136">應用程式沒有足夠的記憶體可完成作業，或者 <em>使用者</em>、 <em>密碼</em>或 <em>網域</em> 至少有一個 null 和一個非 null 值。</span><span class="sxs-lookup"><span data-stu-id="88b46-136">The application does not have enough memory to complete the operation or the <em>user</em>, <em>password</em>, or <em>domain</em> has at least one null and one non-null value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88b46-137">53</span><span class="sxs-lookup"><span data-stu-id="88b46-137">53</span></span></td>
<td><span data-ttu-id="88b46-138">在下列情況下，會傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="88b46-138">This error is returned in the following situations:</span></span>
<ul>
<li><span data-ttu-id="88b46-139"><em>ServerName</em>參數中指定的電腦名稱稱不存在。</span><span class="sxs-lookup"><span data-stu-id="88b46-139">The computer name specified in the <em>serverName</em> parameter does not exist.</span></span></li>
<li><span data-ttu-id="88b46-140">當您嘗試連線到 Windows Server 2003 或 Windows XP 電腦，而且遠端電腦未啟用 [檔案和印表機共用] 防火牆例外，或遠端登入服務未執行時。</span><span class="sxs-lookup"><span data-stu-id="88b46-140">When you are trying to connect to a Windows Server 2003 or Windows XP computer, and the remote computer does not have the File and Printer Sharing firewall exception enabled or the Remote Registry service is not running.</span></span></li>
<li><span data-ttu-id="88b46-141">當您嘗試連線到 Windows Vista 電腦時，如果遠端電腦未啟用 [遠端排程工作] 管理防火牆例外，且已啟用 [檔案及印表機共用] 防火牆例外，或遠端登入服務未執行。</span><span class="sxs-lookup"><span data-stu-id="88b46-141">When you are trying to connect to a Windows Vista computer, and the remote computer does not have the Remote Scheduled Tasks Management firewall exception enabled and the File and Printer Sharing firewall exception enabled, or the Remote Registry service is not running.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88b46-142">50</span><span class="sxs-lookup"><span data-stu-id="88b46-142">50</span></span></td>
<td><span data-ttu-id="88b46-143">從 Windows Vista 電腦連線到遠端 Windows XP 或 Windows Server 2003 電腦時，無法指定 <em>使用者</em>、 <em>密碼</em>或 <em>網域</em> 參數。</span><span class="sxs-lookup"><span data-stu-id="88b46-143">The <em>user</em>, <em>password</em>, or <em>domain</em> parameters cannot be specified when connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="88b46-144">如果您是從 Windows Vista 連接到遠端 Windows Vista 電腦，則需要允許遠端電腦上的遠端排程工作管理防火牆例外。</span><span class="sxs-lookup"><span data-stu-id="88b46-144">If you are to connecting to a remote Windows Vista computer from a Windows Vista, you need to allow the Remote Scheduled Tasks Management firewall exception on the remote computer.</span></span> <span data-ttu-id="88b46-145">若要允許此例外，請依序按一下 [開始]、[控制台]、[安全性]、[允許程式通過 Windows 防火牆]，然後選取 [遠端排程工作管理] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="88b46-145">To allow this exception click Start, Control Panel, Security, Allow a program through Windows Firewall, and then select the Remote Scheduled Tasks Management check box.</span></span> <span data-ttu-id="88b46-146">接著按一下 [Windows 防火牆設定] 對話方塊中的 [確定] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="88b46-146">Then click the Ok button in the Windows Firewall Settings dialog box.</span></span>

<span data-ttu-id="88b46-147">如果您是從 Windows Vista 電腦連線到遠端 Windows XP 或 Windows Server 2003 電腦，則需要允許遠端電腦上的 [檔案及印表機共用] 防火牆例外。</span><span class="sxs-lookup"><span data-stu-id="88b46-147">If you are connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer, you need to allow the File and Printer Sharing firewall exception on the remote computer.</span></span> <span data-ttu-id="88b46-148">若要允許此例外，請依序按一下 [開始]、[控制台]，按兩下 [Windows 防火牆]，選取 [例外] 索引標籤，然後選取 [檔案及印表機共用] 防火牆例外。</span><span class="sxs-lookup"><span data-stu-id="88b46-148">To allow this exception click Start, Control Panel, double-click Windows Firewall, select the Exceptions tab, and then select the File and Printer Sharing firewall exception.</span></span> <span data-ttu-id="88b46-149">然後按一下 [Windows 防火牆] 對話方塊中的 [確定] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="88b46-149">Then click the OK button in the Windows Firewall dialog box.</span></span> <span data-ttu-id="88b46-150">遠端登入服務也必須在遠端電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="88b46-150">The Remote Registry service must also be running on the remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="88b46-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="88b46-151">Requirements</span></span>



| <span data-ttu-id="88b46-152">需求</span><span class="sxs-lookup"><span data-stu-id="88b46-152">Requirement</span></span> | <span data-ttu-id="88b46-153">值</span><span class="sxs-lookup"><span data-stu-id="88b46-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88b46-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88b46-154">Minimum supported client</span></span><br/> | <span data-ttu-id="88b46-155">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88b46-155">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="88b46-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88b46-156">Minimum supported server</span></span><br/> | <span data-ttu-id="88b46-157">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88b46-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="88b46-158">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="88b46-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="88b46-159"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="88b46-159"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="88b46-160">DLL</span><span class="sxs-lookup"><span data-stu-id="88b46-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88b46-161"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88b46-161"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





