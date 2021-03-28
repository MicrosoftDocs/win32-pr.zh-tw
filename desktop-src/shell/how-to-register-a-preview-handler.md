---
description: 本主題說明如何註冊與指定資料類型相關聯的預覽處理常式。
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: 如何註冊預覽處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973132"
---
# <a name="how-to-register-a-preview-handler"></a><span data-ttu-id="8bf56-103">如何註冊預覽處理常式</span><span class="sxs-lookup"><span data-stu-id="8bf56-103">How to Register a Preview Handler</span></span>

<span data-ttu-id="8bf56-104">本主題說明如何註冊與指定資料類型相關聯的預覽處理常式。</span><span class="sxs-lookup"><span data-stu-id="8bf56-104">This topic explains how to register a preview handler associated with a given data type.</span></span> <span data-ttu-id="8bf56-105">為了方便說明，本主題中的範例會使用 .xyz 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8bf56-105">For the purposes of illustration, examples in this topic use a .xyz file type.</span></span> <span data-ttu-id="8bf56-106">註冊預覽處理常式是標準的檔案關聯型註冊。</span><span class="sxs-lookup"><span data-stu-id="8bf56-106">Registration of a preview handler is a standard file association-based registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="8bf56-107">指示</span><span class="sxs-lookup"><span data-stu-id="8bf56-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8bf56-108">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="8bf56-108">Step 1:</span></span>

<span data-ttu-id="8bf56-109">首先，副檔名與 ProgID 相關聯。</span><span class="sxs-lookup"><span data-stu-id="8bf56-109">First, a file name extension is associated with a ProgID.</span></span> <span data-ttu-id="8bf56-110">下列專案會將 **xyzfile** ProgID 子機碼與 .xyz 副檔名產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8bf56-110">The following entry associates the **xyzfile** ProgID subkey with the .xyz file name extension.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

<span data-ttu-id="8bf56-111">**Xyzfile** ProgID 子機碼會與其他 progid 儲存，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8bf56-111">The **xyzfile** ProgID subkey is stored with the other ProgIDs as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
```

<span data-ttu-id="8bf56-112">每個預覽處理常式 ProgID 子機碼都包含名為 **shellex** 的子機碼，其中包含 *名為* **{8895b1c6-b41f-4c1c-a562-0d564250836f}** 的子機</span><span class="sxs-lookup"><span data-stu-id="8bf56-112">Each preview handler ProgID subkey contains a subkey named **shellex** that contains a subkey *always* named **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span></span> <span data-ttu-id="8bf56-113">該子機碼的存在會告訴系統處理常式是預覽處理常式。</span><span class="sxs-lookup"><span data-stu-id="8bf56-113">The presence of that subkey tells the system that the handler is a preview handler.</span></span>

<span data-ttu-id="8bf56-114">**{8895b1c6-b41f-4c1c-a562-0d564250836f}** 子機碼的預設值是處理常式 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bf56-114">The default value of the **{8895b1c6-b41f-4c1c-a562-0d564250836f}** subkey is the class identifier (CLSID) of your handler.</span></span> <span data-ttu-id="8bf56-115">**Xyzfile** ProgID 子機碼的範例如下所示，關聯 CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154} 的處理常式。</span><span class="sxs-lookup"><span data-stu-id="8bf56-115">An example of the **xyzfile** ProgID subkey is shown here, associating a handler of CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a><span data-ttu-id="8bf56-116">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="8bf56-116">Step 2:</span></span>

<span data-ttu-id="8bf56-117">接下來，在預覽處理常式的 [ **CLSID** ] 下新增子機碼。</span><span class="sxs-lookup"><span data-stu-id="8bf56-117">Next, add the subkey under **CLSID** for your preview handler.</span></span> <span data-ttu-id="8bf56-118">範例如下所示。</span><span class="sxs-lookup"><span data-stu-id="8bf56-118">An example is shown here.</span></span> <span data-ttu-id="8bf56-119">以下是個別專案的說明。</span><span class="sxs-lookup"><span data-stu-id="8bf56-119">An explanation of individual entries follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

<span data-ttu-id="8bf56-120">子機碼的預設值 (在此處， **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) 並非必要或使用。</span><span class="sxs-lookup"><span data-stu-id="8bf56-120">The default value for your subkey (here, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) is not required or used.</span></span> <span data-ttu-id="8bf56-121">但是，將其設定為未當地語系化的字串可協助您偵測註冊問題。</span><span class="sxs-lookup"><span data-stu-id="8bf56-121">However, setting it to a nonlocalized string can help you to debug registration issues.</span></span>

<span data-ttu-id="8bf56-122">DisplayName 專案的 .dll 資源中的負號 (-101) 存在於舊版的原因。</span><span class="sxs-lookup"><span data-stu-id="8bf56-122">The minus sign (-101) in the .dll resource in the DisplayName entry exists for legacy reasons.</span></span> <span data-ttu-id="8bf56-123">相反地，圖示專案不需要減號。</span><span class="sxs-lookup"><span data-stu-id="8bf56-123">The Icon entry, on the other hand, does not require a minus sign.</span></span>

<span data-ttu-id="8bf56-124">AppID 值會提供與副檔名相關聯之應用程式的 appid 參考， (儲存在 **HKEY \_ 類別 \_ 根目錄** \\ **AppID** 下。</span><span class="sxs-lookup"><span data-stu-id="8bf56-124">The AppID value gives a reference to the AppID of the application associated with the file name extension (stored under **HKEY\_CLASSES\_ROOT**\\**APPID**.</span></span> <span data-ttu-id="8bf56-125">此處所使用的值（{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}）是 Prevhost.exe 代理主機的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bf56-125">The value used here—{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}—is the ID of the Prevhost.exe surrogate host.</span></span> <span data-ttu-id="8bf56-126">32位預覽處理常式在64位作業系統上安裝時，應使用 **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C}。</span><span class="sxs-lookup"><span data-stu-id="8bf56-126">32-bit preview handlers should use **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} when installed on 64-bit operating systems.</span></span>

<span data-ttu-id="8bf56-127">**InprocServer32** 子機碼底下的專案包含對副檔名之 ProgID 子機碼的參考，以及 [VersionIndependentProgID](../com/versionindependentprogid.md)的專案。</span><span class="sxs-lookup"><span data-stu-id="8bf56-127">The entries under the **InprocServer32** subkey include a reference back to the file name extension's ProgID subkey as well as an entry for a [VersionIndependentProgID](../com/versionindependentprogid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="8bf56-128">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="8bf56-128">Step 3:</span></span>

<span data-ttu-id="8bf56-129">最後，預覽處理常式必須加入至所有預覽處理常式的清單中。</span><span class="sxs-lookup"><span data-stu-id="8bf56-129">Finally, the preview handler must be added to the list of all preview handlers.</span></span> <span data-ttu-id="8bf56-130">這份清單是由系統用來為顯示目的列舉所有已註冊預覽處理常式的優化。</span><span class="sxs-lookup"><span data-stu-id="8bf56-130">This list is used as an optimization by the system to enumerate all registered preview handlers for display purposes.</span></span> <span data-ttu-id="8bf56-131">同樣地，預設值並非必要，它只會輔助偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="8bf56-131">Again, the default value is not required, it simply aids in the debugging process.</span></span>

> [!Note]  
> <span data-ttu-id="8bf56-132">在 Windows 7 中，如果已為電腦的所有使用者安裝應用程式，請使用 HKEY \_ 本機 \_ 電腦; 如果只針對一位使用者，請使用 HKEY \_ 目前的 \_ 使用者。</span><span class="sxs-lookup"><span data-stu-id="8bf56-132">In Windows 7, if the application is installed for all users of the computer, use HKEY\_LOCAL\_MACHINE; if for only one user, use HKEY\_CURRENT\_USER.</span></span>

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a><span data-ttu-id="8bf56-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="8bf56-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bf56-134">預覽處理常式和 Shell 預覽主機</span><span class="sxs-lookup"><span data-stu-id="8bf56-134">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="8bf56-135">建立預覽處理常式</span><span class="sxs-lookup"><span data-stu-id="8bf56-135">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="8bf56-136">預覽處理常式指導方針</span><span class="sxs-lookup"><span data-stu-id="8bf56-136">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
