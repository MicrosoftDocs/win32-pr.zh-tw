---
description: 本節說明如何設定您的環境，以使用 c + + 中的 Tablet PC platform COM 程式庫。
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: COM 程式庫和 ActiveX 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971159"
---
# <a name="com-library-and-activex-controls"></a><span data-ttu-id="e617f-103">COM 程式庫和 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="e617f-103">COM Library and ActiveX Controls</span></span>

<span data-ttu-id="e617f-104">本節說明如何設定您的環境，以使用 c + + 中的 Tablet PC platform COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="e617f-104">This section describes how to set up your environment to use the Tablet PC platform COM libraries in C++.</span></span>

## <a name="microsoft-visual-c"></a><span data-ttu-id="e617f-105">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="e617f-105">Microsoft Visual C++</span></span>

<span data-ttu-id="e617f-106">若要在 Visual C++ 中建立 Tablet PC 應用程式，您必須更新系統內容變數、設定 Visual Studio 的目錄選項，以及存取專案中的 Tablet PC 介面。</span><span class="sxs-lookup"><span data-stu-id="e617f-106">To build Tablet PC applications in Visual C++, you need to update the system environment variables, set up directory options for Visual Studio, and access the Tablet PC interfaces in your project.</span></span>

<span data-ttu-id="e617f-107">若要更新環境變數，請依照 Windows SDK 所提供的指示，將環境變數新增至 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="e617f-107">To update the environment variables, follow the instructions provided by the Windows SDK for adding the environment variables to Visual Studio.</span></span>

### <a name="accessing-the-tablet-pc-interfaces"></a><span data-ttu-id="e617f-108">存取 Tablet PC 介面</span><span class="sxs-lookup"><span data-stu-id="e617f-108">Accessing the Tablet PC Interfaces</span></span>

<span data-ttu-id="e617f-109">若要存取 Tablet PC 介面，您必須在專案中包含 Msinkaut 和 Msinkaut 的 c 檔案。 \_</span><span class="sxs-lookup"><span data-stu-id="e617f-109">To access the Tablet PC interfaces, you must include the Msinkaut.h and Msinkaut\_i.c files in your project.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="e617f-110">您也可以使用下列匯入指示詞，而不是 \# 先前列出的 include 語句。</span><span class="sxs-lookup"><span data-stu-id="e617f-110">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="e617f-111">若要存取 InkAnalysis 介面，您必須 \_ 在專案中包含 IACom .h 和 IACom 檔案。</span><span class="sxs-lookup"><span data-stu-id="e617f-111">To access the InkAnalysis interfaces, you must include IACom.h and IACom\_i.c files in your project.</span></span>


```C++
#include <IACom.h>
#include <IACom_i.c>
```



<span data-ttu-id="e617f-112">您也可以使用下列匯入指示詞，而不是 \# 先前列出的 include 語句。</span><span class="sxs-lookup"><span data-stu-id="e617f-112">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="e617f-113">若要存取 [**InkDivider**](inkdivider-class.md) 介面，您必須 \_ 在專案中包含 msinkaut15 c 和 msinkaut15 .h 檔案。</span><span class="sxs-lookup"><span data-stu-id="e617f-113">To access the [**InkDivider**](inkdivider-class.md) interfaces, you must include msinkaut15\_i.c and msinkaut15.h files in your project.</span></span>

> [!Note]  
> <span data-ttu-id="e617f-114">InkDivider 已被筆墨分析 Api 取代。</span><span class="sxs-lookup"><span data-stu-id="e617f-114">InkDivider has been superseded by the Ink Analysis APIs.</span></span>

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



<span data-ttu-id="e617f-115">您也可以使用下列匯入指示詞，而不是 \# include 語句。</span><span class="sxs-lookup"><span data-stu-id="e617f-115">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="e617f-116">若要存取 [**PenInputPanel**](peninputpanel-class.md) 介面，您必須 \_ 在專案中包含 PenInputPanel c 和 PenInputPanel .h 檔案。</span><span class="sxs-lookup"><span data-stu-id="e617f-116">To access the [**PenInputPanel**](peninputpanel-class.md) interfaces, you must include PenInputPanel\_i.c and PenInputPanel.h files in your project.</span></span>


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



<span data-ttu-id="e617f-117">您也可以使用下列匯入指示詞，而不是 \# include 語句。</span><span class="sxs-lookup"><span data-stu-id="e617f-117">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> <span data-ttu-id="e617f-118">在 Windows Vista 中，PenInputPanel Api 已由新的文字輸入面板介面取代。</span><span class="sxs-lookup"><span data-stu-id="e617f-118">The PenInputPanel APIs have been superseded in Windows Vista by the new Text Input Panel interfaces.</span></span>

 

<span data-ttu-id="e617f-119">若要存取 [InkEdit](inkedit-control-reference.md) 控制項介面，您必須 \_ 在您的專案中包含筆跡 .h 和筆跡檔。</span><span class="sxs-lookup"><span data-stu-id="e617f-119">To access the [InkEdit](inkedit-control-reference.md) Control interfaces, you must include the Inked.h and Inked\_i.c files in your project.</span></span>


```C++
#include <inked.h>
#include <inked_i.c>
```



<span data-ttu-id="e617f-120">或者，您也可以匯 \# 入 InkEd.dll 檔案。</span><span class="sxs-lookup"><span data-stu-id="e617f-120">Alternatively, you can \#import the InkEd.dll file.</span></span>


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



