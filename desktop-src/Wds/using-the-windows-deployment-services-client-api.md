---
title: 使用 Windows 部署服務用戶端 API
description: 在標準 Windows 部署服務 (WDS) 解決方案無法用來安裝 Windows 的環境中，WDS 用戶端的 API 可讓開發人員撰寫自訂部署應用程式。
ms.assetid: abe2a7c7-989a-456e-80df-90d5b816db38
keywords:
- 使用用戶端 API Windows 部署服務 Windows 部署服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 872422a5c84bf1d8ea7c3688b122ba2389c1e968
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023621"
---
# <a name="using-the-windows-deployment-services-client-api"></a>使用 Windows 部署服務用戶端 API

在標準 Windows 部署服務 (WDS) 解決方案無法用來安裝 Windows 的環境中，WDS 用戶端的 API 可讓開發人員撰寫自訂部署應用程式。 應用程式可以使用此 API 與 WDS 伺服器通訊，以取得可從伺服器取得之系統映射的相關資訊。 自訂 WDS 用戶端應用程式應遵循下列指導方針。

## <a name="install-the-wds-role-on-the-server"></a>在伺服器上安裝 WDS 角色

-   Windows 部署服務 (WDS) 是 (RIS) 的遠端安裝服務修訂版本，您將需要伺服器上的 WDS 伺服器角色才能執行自訂 WDS 用戶端解決方案。
-   WDS 會以 Windows Server 2008 和 Windows Server 2003 Service Pack 2 (SP2) 的標準元件取代 RIS。
-   您必須將 RIS 伺服器更新至 Windows Server 2003 Service Pack 1 (SP1) 上的 WDS。 您可以使用 [Windows 自動化安裝套件 (WAIK) ](https://www.microsoft.com/download/details.aspx?id=10333)來安裝 WDS 伺服器角色。

## <a name="start-windows-pe-20"></a>啟動 Windows PE 2。0

必須啟動 Windows PE 2.0 （如果尚未啟動）。 WDS 用戶端和支援的 Dll 只有在安裝程式的 Microsoft Windows 預先安裝環境 (Windows PE 2.0) 階段時，才會由 setup.exe 載入。

-   當新的電腦連線到網路時，內建的開機前執行環境 (PXE) 技術可以用來下載網路開機程式。 如需有關 PXE 啟動電腦以安裝 Windows 的詳細資訊，請參閱 [Windows 部署服務更新逐步指南](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10))。
-   Windows PE 2.0 的 RAMDISK 可開機映射可以儲存在中。WIM 格式，並在網路開機過程中下載。 然後您就可以直接從該媒體載入和執行 Windows PE。

## <a name="open-a-session-with-the-wds-server"></a>開啟與 WDS 伺服器的會話

WDS 用戶端必須開啟與 WDS 伺服器的會話。

-   使用 [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) 函式來開啟與 WDS 伺服器的會話。 此函式會接受伺服器的名稱或 IP 位址，並接收 WDS 用戶端會話的控制碼位址。
-   如果使用伺服器開啟會話將需要驗證 WDS 用戶端，應用程式應該在呼叫 [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession)函式時，提供包含用戶端認證的 [**WDS \_ CLI \_**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)認證結構的位址。 應用程式可以使用 [**WdsCliAuthorizeSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession) 函式，將匿名會話轉換成經過驗證的會話。
-   當不再需要使用 [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) 函式開啟的會話時，應用程式應該使用 [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) 函數來關閉會話所持有的控制碼和釋放資源。

## <a name="enumerate-system-images-on-the-wds-server"></a>列舉 WDS 伺服器上的系統映射

WDS 用戶端可以使用 API 來列舉 WDS 伺服器上的系統映射。

-   您可以使用 [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) 函式來取得第一個映射的控制碼，以及初始化 WDS 伺服器上的映射列舉。
-   使用 [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) 函式來遞增 [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) 函數所啟動的列舉。 **WdsCliFindNextImage** 函式會取得下一個影像的控制碼。
-   您可以使用 [**WdsCliGetImageIndex**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex) 函式來取得目前影像的影像索引。 只有在再次使用 [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) 或 [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) 函式之前，此值才有效。
-   您可以使用 [**WdsCliGetEnumerationFlags**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags) 函數來取得有關影像篩選的資訊旗標。

## <a name="get-information-about-images"></a>取得映射的相關資訊

WDS 用戶端可以使用 API 來取得 WDS 伺服器上映射的相關資訊。 下列函式會取得目前影像的相關資訊。 由於 [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) 和 [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) 函式會變更目前的影像控制碼值，因此應用程式應該儲存它所取得的任何資訊，而且未來將需要這些資訊，才能再次呼叫 **WdsCliFindFirstImage** 或 **WdsCliFindNextImage** 函數。

-   使用 [**WdsCliGetImageArchitecture**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture) 函式取得目前映射的處理器架構。
-   您可以使用 [**WdsCliGetImagePath**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath) 函式來取得包含目前影像之影像檔案的相對路徑。
-   使用 [**WdsCliGetImageSize**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize) 函式來取得影像大小。
-   使用 [**WdsCliGetImageVersion**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion) 函式來取得映射版本。
-   使用 [**WdsCliGetImageLanguage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage) 函式取得目前影像的預設語言。
-   您可以使用 [**WdsCliGetImageLanguages**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages) 函式來取得目前影像所支援的語言陣列。
-   使用 [**WdsCliGetImageLastModifiedTime**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime) 會傳回目前影像的上次修改時間。
-   使用 [**WdsCliGetImageName**](/windows/win32/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename) 函式來取得目前映射的名稱。
-   使用 [**WdsCliGetImageDescription**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription) 函式取得目前影像的描述。
-   使用 [**WdsCliGetImageGroup**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup) 函式來取得目前映射的映射組名。
-   使用 [**WdsCliGetImageHalName**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname) 函式來取得目前映射 (HAL) 名稱的硬體抽象層。

## <a name="log-wds-client-events"></a>記錄 WDS 用戶端事件

WDS 用戶端程式庫的記錄功能可讓您從用戶端將安裝進度事件傳送至 WDS 伺服器。

-   使用 [**WdsCliInitializeLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog) 函式來初始化 WDS 用戶端會話的記錄檔。
-   使用 [**WdsCliLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclilog) 函式將事件訊息寫入至 WDS 伺服器記錄檔。
-   在 Windows Server 2008 上，WDS 伺服器會將用戶端事件寫入應用程式特定事件記錄檔，該記錄檔可透過 eventvwr.exe 以及偵錯工具追蹤記錄檔來查看。 在啟用調試記錄的 Windows Server 2003 上，WDS 伺服器會將用戶端事件寫入至% windir% \\ 追蹤 wdsserver 記錄檔 \\ 。 您必須在伺服器上啟用 WDS 用戶端記錄，才能捕獲這些事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 部署服務 API](about-the-windows-deployment-services-api.md)
</dt> <dt>

[使用 Windows 部署服務伺服器 API](using-the-windows-deployment-services-server-api.md)
</dt> </dl>

 

 