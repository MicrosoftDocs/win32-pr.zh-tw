---
title: CLSID 金鑰
description: CLSID 是識別 COM 類別物件的全域唯一識別碼。 如果您的伺服器或容器允許連結至其内嵌物件，您必須為每個支援的物件類別註冊 CLSID。
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- CLSID 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9253446a039e47996366c7dfdb51c01f9b1993
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372419"
---
# <a name="clsid-key"></a><span data-ttu-id="64571-105">CLSID 金鑰</span><span class="sxs-lookup"><span data-stu-id="64571-105">CLSID Key</span></span>

<span data-ttu-id="64571-106">CLSID 是識別 COM 類別物件的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="64571-106">A CLSID is a globally unique identifier that identifies a COM class object.</span></span> <span data-ttu-id="64571-107">如果您的伺服器或容器允許連結至其内嵌物件，您必須為每個支援的物件類別註冊 CLSID。</span><span class="sxs-lookup"><span data-stu-id="64571-107">If your server or container allows linking to its embedded objects, you need to register a CLSID for each supported class of objects.</span></span>

## <a name="registry-key"></a><span data-ttu-id="64571-108">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="64571-108">Registry Key</span></span>

<span data-ttu-id="64571-109">**HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID** \\ *{* CLSID *}*</span><span class="sxs-lookup"><span data-stu-id="64571-109">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID**\\ *{* CLSID *}*</span></span>



| <span data-ttu-id="64571-110">登錄機碼</span><span class="sxs-lookup"><span data-stu-id="64571-110">Registry key</span></span>                                                 | <span data-ttu-id="64571-111">說明</span><span class="sxs-lookup"><span data-stu-id="64571-111">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64571-112">**AppID**</span><span class="sxs-lookup"><span data-stu-id="64571-112">**AppID**</span></span>](appid.md)                                       | <span data-ttu-id="64571-113">將 AppID 與 CLSID 相關聯。</span><span class="sxs-lookup"><span data-stu-id="64571-113">Associates an AppID with a CLSID.</span></span>                                                                                                        |
| [<span data-ttu-id="64571-114">**AutoConvertTo**</span><span class="sxs-lookup"><span data-stu-id="64571-114">**AutoConvertTo**</span></span>](autoconvertto.md)                       | <span data-ttu-id="64571-115">指定將物件的指定類別自動轉換成物件的新類別。</span><span class="sxs-lookup"><span data-stu-id="64571-115">Specifies the automatic conversion of a given class of objects to a new class of objects.</span></span>                                                |
| [<span data-ttu-id="64571-116">**AutoTreatAs**</span><span class="sxs-lookup"><span data-stu-id="64571-116">**AutoTreatAs**</span></span>](autotreatas.md)                           | <span data-ttu-id="64571-117">自動將 [**TreatAs**](treatas.md) 索引鍵的 CLSID 設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="64571-117">Automatically sets the CLSID for the [**TreatAs**](treatas.md) key to the specified value.</span></span>                                              |
| [<span data-ttu-id="64571-118">**AuxUserType**</span><span class="sxs-lookup"><span data-stu-id="64571-118">**AuxUserType**</span></span>](auxusertype.md)                           | <span data-ttu-id="64571-119">指定應用程式的簡短顯示名稱和應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="64571-119">Specifies an application's short display name and application names.</span></span>                                                                     |
| [<span data-ttu-id="64571-120">**控制**</span><span class="sxs-lookup"><span data-stu-id="64571-120">**Control**</span></span>](control.md)                                   | <span data-ttu-id="64571-121">將物件識別為 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="64571-121">Identifies an object as an ActiveX Control.</span></span>                                                                                              |
| [<span data-ttu-id="64571-122">**轉換**</span><span class="sxs-lookup"><span data-stu-id="64571-122">**Conversion**</span></span>](conversion.md)                             | <span data-ttu-id="64571-123">由 [ **轉換** ] 對話方塊用來判斷應用程式可以讀取和寫入的格式。</span><span class="sxs-lookup"><span data-stu-id="64571-123">Used by the **Convert** dialog box to determine the formats an application can read and write.</span></span>                                           |
| [<span data-ttu-id="64571-124">**DataFormats**</span><span class="sxs-lookup"><span data-stu-id="64571-124">**DataFormats**</span></span>](dataformats.md)                           | <span data-ttu-id="64571-125">指定應用程式所支援的預設和主要資料格式。</span><span class="sxs-lookup"><span data-stu-id="64571-125">Specifies the default and main data formats supported by an application.</span></span>                                                                 |
| [<span data-ttu-id="64571-126">**DefaultIcon**</span><span class="sxs-lookup"><span data-stu-id="64571-126">**DefaultIcon**</span></span>](defaulticon.md)                           | <span data-ttu-id="64571-127">提供 iconic 物件簡報的預設圖示資訊。</span><span class="sxs-lookup"><span data-stu-id="64571-127">Provides default icon information for iconic presentations of objects.</span></span>                                                                   |
| [<span data-ttu-id="64571-128">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="64571-128">**InprocHandler**</span></span>](inprochandler.md)                       | <span data-ttu-id="64571-129">指定應用程式是否使用自訂處理常式。</span><span class="sxs-lookup"><span data-stu-id="64571-129">Specifies whether an application uses a custom handler.</span></span>                                                                                  |
| [<span data-ttu-id="64571-130">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="64571-130">**InprocHandler32**</span></span>](inprochandler32.md)                   | <span data-ttu-id="64571-131">指定應用程式是否使用自訂處理常式。</span><span class="sxs-lookup"><span data-stu-id="64571-131">Specifies whether an application uses a custom handler.</span></span>                                                                                  |
| [<span data-ttu-id="64571-132">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="64571-132">**InprocServer**</span></span>](inprocserver.md)                         | <span data-ttu-id="64571-133">指定同進程伺服器 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="64571-133">Specifies the path to the in-process server DLL.</span></span>                                                                                         |
| [<span data-ttu-id="64571-134">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="64571-134">**InprocServer32**</span></span>](inprocserver32.md)                     | <span data-ttu-id="64571-135">註冊32位的同進程伺服器，並指定伺服器可以在其中執行之單元的執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="64571-135">Registers a 32-bit in-process server and specifies the threading model of the apartment the server can run in.</span></span>                           |
| [<span data-ttu-id="64571-136">**插入**</span><span class="sxs-lookup"><span data-stu-id="64571-136">**Insertable**</span></span>](insertable.md)                             | <span data-ttu-id="64571-137">指出當 COM 容器應用程式使用時，這個類別的物件應該出現在 [ **插入物件** ] 對話方塊清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="64571-137">Indicates that objects of this class should appear in the **Insert Object** dialog box list box when used by COM container applications.</span></span> |
| [<span data-ttu-id="64571-138">**介面**</span><span class="sxs-lookup"><span data-stu-id="64571-138">**Interface**</span></span>](interface.md)                               | <span data-ttu-id="64571-139">選擇性專案，指定相關聯類別 (Iid) 所支援的所有介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="64571-139">An optional entry that specifies all interface IDs (IIDs) supported by the associated class.</span></span>                                             |
| [<span data-ttu-id="64571-140">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="64571-140">**LocalServer**</span></span>](localserver.md)                           | <span data-ttu-id="64571-141">指定16位本機伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="64571-141">Specifies the full path to a 16-bit local server application.</span></span>                                                                            |
| [<span data-ttu-id="64571-142">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="64571-142">**LocalServer32**</span></span>](localserver32.md)                       | <span data-ttu-id="64571-143">指定32位本機伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="64571-143">Specifies the full path to a 32-bit local server application.</span></span>                                                                            |
| [<span data-ttu-id="64571-144">**MiscStatus**</span><span class="sxs-lookup"><span data-stu-id="64571-144">**MiscStatus**</span></span>](miscstatus.md)                             | <span data-ttu-id="64571-145">指定如何建立和顯示物件。</span><span class="sxs-lookup"><span data-stu-id="64571-145">Specifies how to create and display an object.</span></span>                                                                                           |
| [<span data-ttu-id="64571-146">**ProgID**</span><span class="sxs-lookup"><span data-stu-id="64571-146">**ProgID**</span></span>](progid.md)                                     | <span data-ttu-id="64571-147">將 ProgID 與 CLSID 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="64571-147">Associates a ProgID with a CLSID.</span></span>                                                                                                        |
| [<span data-ttu-id="64571-148">**ToolBoxBitmap32**</span><span class="sxs-lookup"><span data-stu-id="64571-148">**ToolBoxBitmap32**</span></span>](toolboxbitmap32.md)                   | <span data-ttu-id="64571-149">識別要用於工具列或工具箱按鈕臉部的 16 x 16 點陣圖的模組名稱和資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="64571-149">Identifies the module name and resource ID for a 16 x 16 bitmap to use for the face of a toolbar or toolbox button.</span></span>                      |
| [<span data-ttu-id="64571-150">**TreatAs**</span><span class="sxs-lookup"><span data-stu-id="64571-150">**TreatAs**</span></span>](treatas.md)                                   | <span data-ttu-id="64571-151">指定可模擬目前類別之類別的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="64571-151">Specifies the CLSID of a class that can emulate the current class.</span></span>                                                                       |
| [<span data-ttu-id="64571-152">**動詞**</span><span class="sxs-lookup"><span data-stu-id="64571-152">**Verb**</span></span>](verb.md)                                         | <span data-ttu-id="64571-153">指定要為應用程式註冊的動詞。</span><span class="sxs-lookup"><span data-stu-id="64571-153">Specifies the verbs to be registered for an application.</span></span>                                                                                 |
| [<span data-ttu-id="64571-154">**版本**</span><span class="sxs-lookup"><span data-stu-id="64571-154">**Version**</span></span>](version.md)                                   | <span data-ttu-id="64571-155">指定控制項的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="64571-155">Specifies the version number of the control.</span></span>                                                                                             |
| [<span data-ttu-id="64571-156">**VersionIndependentProgID**</span><span class="sxs-lookup"><span data-stu-id="64571-156">**VersionIndependentProgID**</span></span>](versionindependentprogid.md) | <span data-ttu-id="64571-157">將 ProgID 與 CLSID 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="64571-157">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="64571-158">此值可用來判斷物件應用程式的最新版本。</span><span class="sxs-lookup"><span data-stu-id="64571-158">This value is used to determine the latest version of an object application.</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="64571-159">備註</span><span class="sxs-lookup"><span data-stu-id="64571-159">Remarks</span></span>

<span data-ttu-id="64571-160">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。</span><span class="sxs-lookup"><span data-stu-id="64571-160">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

<span data-ttu-id="64571-161">CLSID 索引鍵包含當類別處於執行中狀態時，預設 COM 處理常式用來傳回其相關資訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="64571-161">The CLSID key contains information used by the default COM handler to return information about a class when it is in the running state.</span></span>

<span data-ttu-id="64571-162">若要取得應用程式的 CLSID，您可以使用 Uuidgen.exe，或使用 [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) 函數。</span><span class="sxs-lookup"><span data-stu-id="64571-162">To obtain a CLSID for your application, you can use the Uuidgen.exe, or use the [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) function.</span></span>

<span data-ttu-id="64571-163">CLSID 是一對大括弧內的128位數位（以十六進位表示）。</span><span class="sxs-lookup"><span data-stu-id="64571-163">The CLSID is a 128-bit number, in hex, within a pair of curly braces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64571-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="64571-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64571-165">**CoCreateGuid**</span><span class="sxs-lookup"><span data-stu-id="64571-165">**CoCreateGuid**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




