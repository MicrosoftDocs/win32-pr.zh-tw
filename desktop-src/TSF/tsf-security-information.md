---
title: 安全性考慮文字服務架構
description: 安全性考慮文字服務架構
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- 文字服務架構 (TSF) ，安全性
- TSF (文字服務架構) ，安全性
- 文字服務，安全性
- 啟用 TSF 的應用程式，安全性
- TSF 的安全性
- 文字服務架構 (TSF) 、最佳作法
- TSF (文字服務架構) ，最佳作法
- 啟用 TSF 的應用程式，最佳作法
- 文字服務、最佳作法
- TSF 的最佳作法
- 文字服務架構 (TSF) ，錯誤檢查
- TSF (文字服務架構) ，錯誤檢查
- 啟用 TSF 的應用程式，錯誤檢查
- 文字服務，錯誤檢查
- 錯誤檢查
- 文字服務架構 (TSF) 、數位簽章
- TSF (文字服務架構) 、數位簽章
- 文字服務、數位簽章
- 啟用 TSF 的應用程式，數位簽章
- 數位簽章
- 文字服務架構 (TSF) 、LoadLibrary 呼叫
- TSF (文字服務架構) ，LoadLibrary 呼叫
- 文字服務，LoadLibrary 呼叫
- 啟用 TSF 的應用程式，LoadLibrary 呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432418fbcb6221082083d6595aa374939bc2f4d5cf5aad145cac87444e75bdc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873573"
---
# <a name="security-considerations-text-services-framework"></a>安全性考慮：文字服務架構

## <a name="best-practices-for-developing-with-tsf"></a>使用 TSF 進行開發的最佳作法

-   **數位簽章：** 文字服務提供者應該提供數位簽章給其二進位可執行檔。 註冊的文字服務可以存取系統執行緒，而且可能會公開其他無法存取的資訊。 為了協助確保穩定且安全的作業，使用者應該先驗證文字服務的數位簽章，然後才允許文字服務載入。 請參閱程式 [代碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) ，以取得建立數位簽章的適當程式。
-   **檢查錯誤：** 應檢查每個方法或函數呼叫是否成功。 如果發生失敗，則應該略過其餘的方法或函式呼叫。 本檔中的大部分程式碼範例都有限制的錯誤檢查，或是完全不會發生的問題，以避免遮蔽所要說明的點。 您不應該將範例直接從檔貼入生產程式碼;相反地，您應該新增自己的錯誤檢查來增強範例。

-   **LoadLibrary 呼叫：** 若要取得任何 [TSF](text-services-framework-functions.md)函式的指標，您將需要使用 [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)。 不過，請務必遵循 **LoadLibrary** 檔中所提供的格式設定 DLL 路徑名稱的程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[安全性最佳作法](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[TSF 函式](text-services-framework-functions.md)
</dt> <dt>

[LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 