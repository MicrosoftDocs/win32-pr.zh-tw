---
description: 此程式會檢查 MicrosoftTablet 電腦和觸控技術核心元件的存在和設定。
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Tablet PC 平臺資訊範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d815f21233b1edcc90d456df68b3736c170a5fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990438"
---
# <a name="tablet-pc-platform-info-sample"></a><span data-ttu-id="2cf36-103">Tablet PC 平臺資訊範例</span><span class="sxs-lookup"><span data-stu-id="2cf36-103">Tablet PC Platform Info Sample</span></span>

<span data-ttu-id="2cf36-104">此程式會檢查 MicrosoftTablet 電腦和觸控技術核心元件的存在和設定。</span><span class="sxs-lookup"><span data-stu-id="2cf36-104">This program checks the presence and configuration of the MicrosoftTablet PC and Touch Technology core components.</span></span> <span data-ttu-id="2cf36-105">它會決定是否在作業系統中啟用 Tablet PC 元件、列出核心控制項的名稱和版本資訊，以及預設的手寫和語音辨識器。</span><span class="sxs-lookup"><span data-stu-id="2cf36-105">It determines whether Tablet PC components are enabled in the operating system, listing names and version information for core controls and the default handwriting and speech recognizer.</span></span>

<span data-ttu-id="2cf36-106">應用程式會使用 GetSystemMetrics Windows API （傳入 SM \_ 平板電腦）來判斷是否在 Tablet PC 上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2cf36-106">The application uses the GetSystemMetrics Windows API, passing in SM\_TABLETPC, to determine whether the application running on a Tablet PC.</span></span> <span data-ttu-id="2cf36-107">SM \_ 平板電腦定義于 WinUser 中。</span><span class="sxs-lookup"><span data-stu-id="2cf36-107">SM\_TABLETPC is defined in WinUser.h.</span></span>

<span data-ttu-id="2cf36-108">特別重要的是，應用程式使用辨識器集合來提供預設辨識器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2cf36-108">Of particular interest is the way the application uses the Recognizers collection to provide information about the default recognizer.</span></span> <span data-ttu-id="2cf36-109">在嘗試使用辨識器集合和辨識器物件之前，應用程式會先測試是否成功建立。</span><span class="sxs-lookup"><span data-stu-id="2cf36-109">Before attempting to use the Recognizers collection and Recognizer object, the application tests for their successful creation.</span></span>

## <a name="components"></a><span data-ttu-id="2cf36-110">單元</span><span class="sxs-lookup"><span data-stu-id="2cf36-110">Components</span></span>

<span data-ttu-id="2cf36-111">使用可轉散發合併模組，Tablet PC 平臺 API 的某些部分可能會安裝在 Vista 和 Windows XP Professional 的非平板電腦版本上。</span><span class="sxs-lookup"><span data-stu-id="2cf36-111">Using the re-distributable merge module, certain parts of the Tablet PC Platform API may be installed on non-Tablet versions of Vista and Windows XP Professional .</span></span> <span data-ttu-id="2cf36-112">GetSystemMetrics 呼叫只會指出已安裝 Windows XP Tablet PC Edition。</span><span class="sxs-lookup"><span data-stu-id="2cf36-112">The GetSystemMetrics call only indicates that Windows XP Tablet PC Edition is installed.</span></span> <span data-ttu-id="2cf36-113">應用程式應該一律判斷指定的元件是否可用。</span><span class="sxs-lookup"><span data-stu-id="2cf36-113">An application should always determine if a given component is available.</span></span> <span data-ttu-id="2cf36-114">若要判斷是否已安裝 API 的元件，正確的方式是嘗試建立物件或控制項的實例，並在嘗試使用它之前檢查它是否存在，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="2cf36-114">The proper way to determine if a component of the API is installed is to attempt to create an instance of an object or control and check that it exists before attempting to use it, as shown in the following example.</span></span>


```C++
IInkRecognizers* pIInkRecognizers = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkRecognizers,
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IInkRecognizers, 
                              (void **)&pIInkRecognizers);
if (SUCCEEDED(hr)) 
{
  // use the component
} else
{
  // component unavailable
}
```



<span data-ttu-id="2cf36-115">應用程式會藉由查看適當的登錄機碼，找出已安裝的語音元件：</span><span class="sxs-lookup"><span data-stu-id="2cf36-115">The application finds out about the installed speech components by looking in the appropriate registry key:</span></span>


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



<span data-ttu-id="2cf36-116">使用 RegQueryValueExW 讀取金鑰。</span><span class="sxs-lookup"><span data-stu-id="2cf36-116">The key is read using RegQueryValueExW.</span></span>

<span data-ttu-id="2cf36-117">最後，此範例會找出已安裝的控制項。</span><span class="sxs-lookup"><span data-stu-id="2cf36-117">Finally, the sample finds out which controls are installed.</span></span>


```C++
LPCOLESTR gc_wszProgId[NUM_CONTROLS] = {L"InkEd.InkEdit", L"msinkaut.InkOverlay"};
// ...
for (int i = 0, j = 0; i < NUM_CONTROLS; i++)
{
    // Get the component info
    CLSID clsid;
    if (SUCCEEDED(CLSIDFromProgID(gc_wszProgId[i], &clsid)) && GetComponentInfo(clsid, info) == TRUE)
    {
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][0], info.wchName);
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][1], info.wchVersion);
        j++;
    }
}
```



 

 



