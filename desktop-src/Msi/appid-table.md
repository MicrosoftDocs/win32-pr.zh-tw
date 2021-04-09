---
description: AppId 資料表或登錄表指定安裝程式在安裝期間設定並註冊 DCOM 伺服器，以執行下列其中一項動作。
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: AppId 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848977"
---
# <a name="appid-table"></a><span data-ttu-id="eb1b7-103">AppId 資料表</span><span class="sxs-lookup"><span data-stu-id="eb1b7-103">AppId Table</span></span>

<span data-ttu-id="eb1b7-104">AppId 資料表或登錄 [表](registry-table.md) 指定安裝程式在安裝期間設定並註冊 DCOM 伺服器，以執行下列其中一項動作。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-104">The AppId table or the [Registry table](registry-table.md) specifies that the installer configure and register DCOM servers to do one of the following during an installation.</span></span>

-   <span data-ttu-id="eb1b7-105">在與啟用伺服器的使用者不同的身分識別下執行 DCOM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-105">Run the DCOM server under a different identity than the user activating the server.</span></span> <span data-ttu-id="eb1b7-106">例如，將 DCOM 伺服器設定為一律以互動式使用者或預先定義使用者的形式執行。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-106">For example, to configure a DCOM server to always run as an interactive user or as a predefined user.</span></span>
-   <span data-ttu-id="eb1b7-107">以服務形式執行 DCOM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-107">Run the DCOM server as a service.</span></span>
-   <span data-ttu-id="eb1b7-108">設定 DCOM 伺服器的預設安全性存取權。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-108">Configure the default security access for the DCOM server.</span></span>
-   <span data-ttu-id="eb1b7-109">註冊 DCOM 伺服器，使其在不同的電腦上啟用。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-109">Register the DCOM server such that it is activated on a different computer.</span></span>

<span data-ttu-id="eb1b7-110">此資料表會在與 [類別] 資料表的 [元件] 資料行中 DCOM 伺服器相關聯的元件安裝時進行處理 \_ 。 [](class-table.md)</span><span class="sxs-lookup"><span data-stu-id="eb1b7-110">This table is processed at the installation of the component associated with the DCOM server in the \_Component column of the [Class table](class-table.md).</span></span> <span data-ttu-id="eb1b7-111">未公告 AppId。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-111">An AppId is not advertised.</span></span>

<span data-ttu-id="eb1b7-112">AppId 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-112">The AppId table has the following columns.</span></span>



| <span data-ttu-id="eb1b7-113">Column</span><span class="sxs-lookup"><span data-stu-id="eb1b7-113">Column</span></span>               | <span data-ttu-id="eb1b7-114">類型</span><span class="sxs-lookup"><span data-stu-id="eb1b7-114">Type</span></span>                       | <span data-ttu-id="eb1b7-115">答案</span><span class="sxs-lookup"><span data-stu-id="eb1b7-115">Key</span></span> | <span data-ttu-id="eb1b7-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="eb1b7-116">Nullable</span></span> |
|----------------------|----------------------------|-----|----------|
| <span data-ttu-id="eb1b7-117">AppId</span><span class="sxs-lookup"><span data-stu-id="eb1b7-117">AppId</span></span>                | [<span data-ttu-id="eb1b7-118">GUID</span><span class="sxs-lookup"><span data-stu-id="eb1b7-118">GUID</span></span>](guid.md)           | <span data-ttu-id="eb1b7-119">Y</span><span class="sxs-lookup"><span data-stu-id="eb1b7-119">Y</span></span>   | <span data-ttu-id="eb1b7-120">N</span><span class="sxs-lookup"><span data-stu-id="eb1b7-120">N</span></span>        |
| <span data-ttu-id="eb1b7-121">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="eb1b7-121">RemoteServerName</span></span>     | [<span data-ttu-id="eb1b7-122">格式 化</span><span class="sxs-lookup"><span data-stu-id="eb1b7-122">Formatted</span></span>](formatted.md) | <span data-ttu-id="eb1b7-123">N</span><span class="sxs-lookup"><span data-stu-id="eb1b7-123">N</span></span>   | <span data-ttu-id="eb1b7-124">Y</span><span class="sxs-lookup"><span data-stu-id="eb1b7-124">Y</span></span>        |
| <span data-ttu-id="eb1b7-125">LocalService</span><span class="sxs-lookup"><span data-stu-id="eb1b7-125">LocalService</span></span>         | [<span data-ttu-id="eb1b7-126">Text</span><span class="sxs-lookup"><span data-stu-id="eb1b7-126">Text</span></span>](text.md)           | <span data-ttu-id="eb1b7-127">N</span><span class="sxs-lookup"><span data-stu-id="eb1b7-127">N</span></span>   | <span data-ttu-id="eb1b7-128">Y</span><span class="sxs-lookup"><span data-stu-id="eb1b7-128">Y</span></span>        |
| <span data-ttu-id="eb1b7-129">ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="eb1b7-129">ServiceParameters</span></span>    | [<span data-ttu-id="eb1b7-130">Text</span><span class="sxs-lookup"><span data-stu-id="eb1b7-130">Text</span></span>](text.md)           | <span data-ttu-id="eb1b7-131">N</span><span class="sxs-lookup"><span data-stu-id="eb1b7-131">N</span></span>   | <span data-ttu-id="eb1b7-132">Y</span><span class="sxs-lookup"><span data-stu-id="eb1b7-132">Y</span></span>        |
| <span data-ttu-id="eb1b7-133">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="eb1b7-133">DllSurrogate</span></span>         | [<span data-ttu-id="eb1b7-134">Text</span><span class="sxs-lookup"><span data-stu-id="eb1b7-134">Text</span></span>](text.md)           | <span data-ttu-id="eb1b7-135">N</span><span class="sxs-lookup"><span data-stu-id="eb1b7-135">N</span></span>   | <span data-ttu-id="eb1b7-136">Y</span><span class="sxs-lookup"><span data-stu-id="eb1b7-136">Y</span></span>        |
| <span data-ttu-id="eb1b7-137">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="eb1b7-137">ActivateAtStorage</span></span>    | [<span data-ttu-id="eb1b7-138">整數</span><span class="sxs-lookup"><span data-stu-id="eb1b7-138">Integer</span></span>](integer.md)     | <span data-ttu-id="eb1b7-139">N</span><span class="sxs-lookup"><span data-stu-id="eb1b7-139">N</span></span>   | <span data-ttu-id="eb1b7-140">Y</span><span class="sxs-lookup"><span data-stu-id="eb1b7-140">Y</span></span>        |
| <span data-ttu-id="eb1b7-141">RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="eb1b7-141">RunAsInteractiveUser</span></span> | [<span data-ttu-id="eb1b7-142">整數</span><span class="sxs-lookup"><span data-stu-id="eb1b7-142">Integer</span></span>](integer.md)     | <span data-ttu-id="eb1b7-143">N</span><span class="sxs-lookup"><span data-stu-id="eb1b7-143">N</span></span>   | <span data-ttu-id="eb1b7-144">Y</span><span class="sxs-lookup"><span data-stu-id="eb1b7-144">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="eb1b7-145">資料行</span><span class="sxs-lookup"><span data-stu-id="eb1b7-145">Columns</span></span>

<dl> <dt>

<span data-ttu-id="eb1b7-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span><span class="sxs-lookup"><span data-stu-id="eb1b7-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span></span>
</dt> <dd>

<span data-ttu-id="eb1b7-147">[類別資料表](class-table.md)的 appid 資料行是 appid 資料表中這個資料行的外鍵。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-147">The AppId column of the [Class table](class-table.md) is a foreign key into this column of the AppId table.</span></span> <span data-ttu-id="eb1b7-148">此資料行包含 AppId 值，將會以 CLSID 撰寫，並在 HKCR appid 下建立 AppId GUID 金鑰 \\ 。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-148">This column contains the AppId value that will be written under the CLSID and creates the AppId GUID key under HKCR\\AppId.</span></span>

</dd> <dt>

<span data-ttu-id="eb1b7-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="eb1b7-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span></span>
</dt> <dd>

<span data-ttu-id="eb1b7-150">此資料行包含 "RemoteServerName" = 的值 <xxxx> ，將會寫入 HKCR \\ AppID \\ {AppID} \\ 。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-150">This column contains the value of "RemoteServerName"=<xxxx> that will be written under HKCR\\AppID\\{AppID}\\ .</span></span>

</dd> <dt>

<span data-ttu-id="eb1b7-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span><span class="sxs-lookup"><span data-stu-id="eb1b7-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span></span>
</dt> <dd>

<span data-ttu-id="eb1b7-152">此資料行包含將在 HKCR \\ AppID \\ { <appid> } "LocalService" = 下寫入的 LocalService 值 <xxx> 。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-152">This column contains the value of LocalService that will be written under HKCR\\AppID\\{<appid>} "LocalService"=<xxx>.</span></span>

</dd> <dt>

<span data-ttu-id="eb1b7-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="eb1b7-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span></span>
</dt> <dd>

<span data-ttu-id="eb1b7-154">此資料行包含將在 HKCR \\ AppID \\ {AppID>} "ServiceParameters" 下寫入的 ServiceParameters 值。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-154">This column contains the value of ServiceParameters that will be written under HKCR\\AppID\\{appid>} "ServiceParameters".</span></span>

</dd> <dt>

<span data-ttu-id="eb1b7-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="eb1b7-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span></span>
</dt> <dd>

<span data-ttu-id="eb1b7-156">此資料行包含將在 HKCR \\ AppId \\ { <appid> } "DllSurrogate" = 下寫入的 DllSurrogate 值 <xxx> 。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-156">This column contains the value of DllSurrogate that will be written under HKCR\\AppId\\{<appid>} "DllSurrogate"=<xxx>.</span></span> <span data-ttu-id="eb1b7-157">如果此資料行存在，則通常會是空字串。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-157">If this column is present it will typically be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="eb1b7-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="eb1b7-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span></span>
</dt> <dd>

<span data-ttu-id="eb1b7-159">此欄位中的非零整數值會導致 Windows Installer 將 HKCR \\ AppID \\ { <appid> } "ActivateAtStorage" = "Y" 寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-159">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{<appid>} "ActivateAtStorage"="Y" into the registry.</span></span> <span data-ttu-id="eb1b7-160">如果欄位是空的，或值為零，則不會寫入任何值。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-160">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> <dt>

<span data-ttu-id="eb1b7-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="eb1b7-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span></span>
</dt> <dd>

<span data-ttu-id="eb1b7-162">此欄位中的非零整數值會導致 Windows Installer 將 HKCR \\ AppID \\ {AppID>} "RunAs" = "Interactive User" 寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-162">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{appid>} "RunAs"="Interactive User" into the registry.</span></span> <span data-ttu-id="eb1b7-163">如果欄位是空的，或值為零，則不會寫入任何值。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-163">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb1b7-164">備註</span><span class="sxs-lookup"><span data-stu-id="eb1b7-164">Remarks</span></span>

<span data-ttu-id="eb1b7-165">[RegisterClassInfo 動作](registerclassinfo-action.md)和[UnregisterClassInfo 動作](unregisterclassinfo-action.md)會使用此資料表。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-165">This table is used by the [RegisterClassInfo action](registerclassinfo-action.md) and [UnregisterClassInfo action](unregisterclassinfo-action.md).</span></span>

<span data-ttu-id="eb1b7-166">請注意，AppId 資料表沒有註冊預設名稱的資料行。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-166">Note that the AppId table does not have a column for registering a Default name.</span></span> <span data-ttu-id="eb1b7-167">因此，如果您需要撰寫使用者易記名稱做為預設的名稱值，就必須使用登錄 [資料表](registry-table.md)進行註冊。</span><span class="sxs-lookup"><span data-stu-id="eb1b7-167">Therefore in cases where you need to write a user friendly name as the Default name value, you must register using the [Registry table](registry-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="eb1b7-168">驗證</span><span class="sxs-lookup"><span data-stu-id="eb1b7-168">Validation</span></span>

<dl>

[<span data-ttu-id="eb1b7-169">ICE03</span><span class="sxs-lookup"><span data-stu-id="eb1b7-169">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="eb1b7-170">ICE06</span><span class="sxs-lookup"><span data-stu-id="eb1b7-170">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="eb1b7-171">ICE32</span><span class="sxs-lookup"><span data-stu-id="eb1b7-171">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="eb1b7-172">ICE33</span><span class="sxs-lookup"><span data-stu-id="eb1b7-172">ICE33</span></span>](ice33.md)  
[<span data-ttu-id="eb1b7-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="eb1b7-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="eb1b7-174">ICE69</span><span class="sxs-lookup"><span data-stu-id="eb1b7-174">ICE69</span></span>](ice69.md)  
</dl>

 

 



