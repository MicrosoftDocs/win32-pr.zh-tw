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
# <a name="functions-designed-to-generate-ui"></a>設計用來產生 UI 的函式

基於範例的目的，應用程式會呼叫 TAPI [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) 函式，該函式是設計來開啟對話方塊，以允許設定與指定線路裝置相關的服務提供者選項。 為了回應此呼叫，TAPI 要求 TAPISRV 呼叫電話語音服務提供者中的 [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) ，以取得 TSP UI DLL 的名稱。

在應用程式的內容中，TAPI 會載入 TSP UI DLL，並使用應用程式所提供的參數來呼叫 [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) 函式，並包含 TAPI [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) 函式的指標。 TSP UI DLL 會顯示 [設定] 對話方塊，視需要呼叫 *DllCallbackProc* 函式，以從電話語音服務提供者取得要顯示的資訊。 每次呼叫 *DllCallbackProc* 函式時，TAPI 要求 TAPISRV 以呼叫電話語音服務提供者的 [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) 函式，從 UI dll 傳入參數區塊，然後將參數區塊傳回至 ui dll。 UI DLL 會呼叫 *DllCallbackProc*，以將任何設定變更傳達給電話語音服務提供者。

當函式完成時，UI DLL 會在此情況下從 (傳回) [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)。 TAPI 會呼叫 [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) 函式來釋放 UI DLL，並將其傳回給應用程式。

 

 
