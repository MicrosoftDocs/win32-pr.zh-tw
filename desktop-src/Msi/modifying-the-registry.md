---
description: 當所有選取的元件及其相關檔案都已安裝之後，就可以將登錄機碼寫入系統登錄。
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: 修改登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320387"
---
# <a name="modifying-the-registry"></a><span data-ttu-id="0f3cc-103">修改登錄</span><span class="sxs-lookup"><span data-stu-id="0f3cc-103">Modifying the Registry</span></span>

<span data-ttu-id="0f3cc-104">當所有選取的元件及其相關檔案都已安裝之後，就可以將登錄機碼寫入系統登錄。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-104">Registry keys can be written to the system registry once all selected components and their related files have been installed.</span></span> <span data-ttu-id="0f3cc-105">與修改登錄相關的標準動作必須在檔案安裝標準動作之後進行排序，因為除非已成功安裝對應的元件和檔案，否則無法寫入登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-105">The standard actions related to modifying the registry must be sequenced after the file installation standard actions because registry keys cannot be written unless the corresponding component and file have been successfully installed.</span></span>

<span data-ttu-id="0f3cc-106">[RegisterClassInfo 動作](registerclassinfo-action.md)會存取[類別資料表](class-table.md)，以註冊已安裝元件的 COM 類別資訊。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-106">The [RegisterClassInfo action](registerclassinfo-action.md) accesses the [Class table](class-table.md) to register the COM class information of the installed components.</span></span>

<span data-ttu-id="0f3cc-107">[RegisterExtensionInfo 動作](registerextensioninfo-action.md)會查詢[延伸模組資料表](extension-table.md)和[動詞資料表](verb-table.md)，並向作業系統註冊對應的擴充功能和命令動詞資訊。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-107">The [RegisterExtensionInfo action](registerextensioninfo-action.md) queries the [Extension table](extension-table.md) and [Verb table](verb-table.md) and registers the corresponding extensions and command-verb information with the operating system.</span></span>

<span data-ttu-id="0f3cc-108">[RegisterProgIdInfo 動作](registerprogidinfo-action.md)會管理 OLE ProgId 資訊與作業系統的註冊。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-108">The [RegisterProgIdInfo action](registerprogidinfo-action.md) manages the registration of OLE ProgId information with the operating system.</span></span>

<span data-ttu-id="0f3cc-109">[RegisterMIMEInfo 動作](registermimeinfo-action.md)會處理[mime 資料表](mime-table.md)，以註冊 mime 內容類型、副檔名和 CLSID 之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-109">The [RegisterMIMEInfo action](registermimeinfo-action.md) processes the [MIME table](mime-table.md) to register the association between a MIME context type, the file name extension, and the CLSID.</span></span>

<span data-ttu-id="0f3cc-110">[WriteRegistryValues 動作](writeregistryvalues-action.md)會處理登錄[表](registry-table.md)，並寫入已安裝在本機或從來源執行之所有元件的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-110">The [WriteRegistryValues action](writeregistryvalues-action.md) processes the [Registry table](registry-table.md) and writes the keys for all components that have been either installed locally or to run from source.</span></span> <span data-ttu-id="0f3cc-111">登錄資料表可讓您將金鑰寫入 **HKEY \_ 類別 \_ ROOT**、 **HKEY \_ CURRENT \_ USER**、 **HKEY \_ LOCAL \_ MACHINE** 和 **HKEY \_ USERS** Registry hive。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-111">The Registry table allows keys to be written to the **HKEY\_CLASSES\_ROOT**, **HKEY\_CURRENT\_USER**, **HKEY\_LOCAL\_MACHINE**, and **HKEY\_USERS** registry hives.</span></span>

<span data-ttu-id="0f3cc-112">[RemoveRegistryValues 動作](removeregistryvalues-action.md)會移除已標示為要在登錄[資料表](registry-table.md)的 [名稱] 資料行或[RemoveRegistry 資料表](removeregistry-table.md)中刪除的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-112">The [RemoveRegistryValues action](removeregistryvalues-action.md) removes the keys that have been marked to be deleted in the Name column of the [Registry table](registry-table.md) or the [RemoveRegistry Table](removeregistry-table.md).</span></span>

<span data-ttu-id="0f3cc-113">[RegisterTypeLibraries 動作](registertypelibraries-action.md)會處理[TypeLib 資料表](typelib-table.md)，並向系統註冊已安裝的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="0f3cc-113">The [RegisterTypeLibraries action](registertypelibraries-action.md) processes the [TypeLib table](typelib-table.md) and registers the installed type libraries with the system.</span></span>

 

 



