---
title: 介面註冊檔案
description: 介面註冊檔案會收集可協助您註冊封裝至 DLL 或 EXE 檔案之 COM 介面的資訊。
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- 介面註冊檔 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966239"
---
# <a name="the-interface-registration-file"></a><span data-ttu-id="9b1c0-104">介面註冊檔案</span><span class="sxs-lookup"><span data-stu-id="9b1c0-104">The Interface Registration File</span></span>

<span data-ttu-id="9b1c0-105">介面註冊檔案會收集可協助您註冊封裝至 DLL 或 EXE 檔案之 COM 介面的資訊。</span><span class="sxs-lookup"><span data-stu-id="9b1c0-105">The interface registration file collects information that helps in the registration of COM interfaces packaged into a DLL or EXE file.</span></span> <span data-ttu-id="9b1c0-106">介面註冊檔案與其他產生的檔案不同，因為它可以從編譯數個不同的 IDL 檔案收集資訊。</span><span class="sxs-lookup"><span data-stu-id="9b1c0-106">The interface registration file is different from other generated files because it can gather information from compiling several different IDL files.</span></span> <span data-ttu-id="9b1c0-107">COM 介面執行的每個 MIDL 編譯器會先尋找現有的 dlldata.c .c 檔案，如果找不到該檔案，就會建立新的 dlldata.c .c 檔案。</span><span class="sxs-lookup"><span data-stu-id="9b1c0-107">Each MIDL compiler run for COM interfaces looks for an existing dlldata.c file first, and if the file is not found, a new dlldata.c file is created.</span></span> <span data-ttu-id="9b1c0-108">如果找到 dlldata.c 檔案，則會將目前 IDL 的相關資訊新增 (如果) 或已取代。</span><span class="sxs-lookup"><span data-stu-id="9b1c0-108">If a dlldata.c file is found, information about the current IDL is added (if absent) or replaced.</span></span>

<span data-ttu-id="9b1c0-109">介面註冊檔會在多處理器環境中安全地產生或更新，因為平行 MIDL 編譯無法同時寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="9b1c0-109">The interface registration file is safely generated or updated in a multiprocessor environment because parallel MIDL compiles are prevented from writing to the file at the same time.</span></span> <span data-ttu-id="9b1c0-110">因為任何 dlldata.c 檔都可以由組建環境或使用者標記為唯讀，所以 MIDL 編譯器會執行超時方法來等候無法開啟的檔案，並在超時時間過期時發出適當的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="9b1c0-110">Because any dlldata.c file can be marked as read-only by either the build environment or the user, the MIDL compiler implements a timeout approach to waiting on a file it cannot open, and issues an appropriate error message if the timeout expires.</span></span>

<span data-ttu-id="9b1c0-111">從輸入檔產生之介面註冊檔的預設名稱是 dlldata.c。</span><span class="sxs-lookup"><span data-stu-id="9b1c0-111">The default name for the interface registration file generated from an input file is dlldata.c.</span></span> <span data-ttu-id="9b1c0-112">[**/Dlldata**](-dlldata.md) MIDL 編譯器參數可以用來覆寫檔案的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="9b1c0-112">The [**/dlldata**](-dlldata.md) MIDL compiler switch can be used to override the default name of the file.</span></span> <span data-ttu-id="9b1c0-113">當封裝至通用二進位檔的某些 IDL 檔案位於不同的目錄時，覆寫介面註冊檔案的預設名稱特別有用。</span><span class="sxs-lookup"><span data-stu-id="9b1c0-113">Overriding the default name of the interface registration file is especially useful when some IDL files packaged to a common binary reside in different directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b1c0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b1c0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b1c0-115">建立和註冊 Proxy DLL</span><span class="sxs-lookup"><span data-stu-id="9b1c0-115">Building and Registering a Proxy DLL</span></span>](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 