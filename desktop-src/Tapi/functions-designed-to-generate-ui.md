---
description: 基於範例的目的，應用程式會呼叫 TAPI lineConfigDialog 函式，該函式是設計來開啟對話方塊，以允許設定與指定線路裝置相關的服務提供者選項。
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: 設計用來產生 UI 的函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa360effd2a1504d2325be2131c430664f1e7a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943437"
---
# <a name="functions-designed-to-generate-ui"></a><span data-ttu-id="8047b-103">設計用來產生 UI 的函式</span><span class="sxs-lookup"><span data-stu-id="8047b-103">Functions Designed to Generate UI</span></span>

<span data-ttu-id="8047b-104">基於範例的目的，應用程式會呼叫 TAPI [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) 函式，該函式是設計來開啟對話方塊，以允許設定與指定線路裝置相關的服務提供者選項。</span><span class="sxs-lookup"><span data-stu-id="8047b-104">Assume for the purposes of an example that the application calls the TAPI [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) function, which is designed to open a dialog box to allow configuration of service provider options related to the specified line device.</span></span> <span data-ttu-id="8047b-105">為了回應此呼叫，TAPI 要求 TAPISRV 呼叫電話語音服務提供者中的 [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) ，以取得 TSP UI DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8047b-105">In response to this call, TAPI requests TAPISRV to call [**TSPI\_providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) in the telephony service provider, obtaining the name of the TSP UI DLL.</span></span>

<span data-ttu-id="8047b-106">在應用程式的內容中，TAPI 會載入 TSP UI DLL，並使用應用程式所提供的參數來呼叫 [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) 函式，並包含 TAPI [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) 函式的指標。</span><span class="sxs-lookup"><span data-stu-id="8047b-106">In the application's context, TAPI loads the TSP UI DLL and calls the [**TUISPI\_lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) function with the parameters supplied by the application, and including a pointer to the TAPI [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) function.</span></span> <span data-ttu-id="8047b-107">TSP UI DLL 會顯示 [設定] 對話方塊，視需要呼叫 *DllCallbackProc* 函式，以從電話語音服務提供者取得要顯示的資訊。</span><span class="sxs-lookup"><span data-stu-id="8047b-107">The TSP UI DLL displays the configuration dialog box, calling the *DllCallbackProc* function as necessary to obtain from the telephony service provider the information to display.</span></span> <span data-ttu-id="8047b-108">每次呼叫 *DllCallbackProc* 函式時，TAPI 要求 TAPISRV 以呼叫電話語音服務提供者的 [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) 函式，從 UI dll 傳入參數區塊，然後將參數區塊傳回至 ui dll。</span><span class="sxs-lookup"><span data-stu-id="8047b-108">Each time the *DllCallbackProc* function is called, TAPI requests TAPISRV to call the telephony service provider's [**TSPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) function, passing in the parameter block from the UI DLL, and returning the parameter block to the UI DLL.</span></span> <span data-ttu-id="8047b-109">UI DLL 會呼叫 *DllCallbackProc*，以將任何設定變更傳達給電話語音服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8047b-109">The UI DLL conveys any configuration changes to the telephony service provider by calling *DllCallbackProc*.</span></span>

<span data-ttu-id="8047b-110">當函式完成時，UI DLL 會在此情況下從 (傳回) [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)。</span><span class="sxs-lookup"><span data-stu-id="8047b-110">When the function is complete, the UI DLL returns from (in this case) [**TUISPI\_lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog).</span></span> <span data-ttu-id="8047b-111">TAPI 會呼叫 [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) 函式來釋放 UI DLL，並將其傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="8047b-111">TAPI calls the [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) function to release the UI DLL, and returns to the application.</span></span>

 

 
