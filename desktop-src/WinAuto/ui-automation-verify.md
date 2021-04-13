---
title: '消費者介面自動化確認 (UIA 確認) '
description: 消費者介面自動化確認 (UIA 確認) 是測試架構，適用于手動和自動化測試 Microsoft 消費者介面自動化的控制項或應用程式的執行。
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- 使用者介面自動化確認
- UIA 確認
- 消費者介面自動化的實作為測試
- 測試消費者介面自動化
- UIA 測試控管
- 消費者介面自動化測試控管
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374614"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>協助工具工具-消費者介面自動化確認 (UIA 確認) 

**消費者介面自動化確認 (UIA 確認)** 是測試架構，適用于手動和自動化測試 Microsoft 消費者介面自動化的控制項或應用程式的執行。 測試架構的大部分功能都是來自稱為 WUIATestLibrary.dll 的 DLL。 此 DLL 包含測試特定消費者介面自動化功能的程式碼，也支援記錄測試結果。 您可以將應用程式整合到測試程式碼中，並定期進行自動化測試或消費者介面自動化案例的點檢查。

**UIA 確認** 已隨 WINDOWS 軟體開發套件 (SDK) 安裝。 它位於 \\ \\ < SDK 安裝路徑的 bin *version* > \\ < *platform* > \\ UIAVerify 資料夾中 (VisualUIAVerifyNative.exe) 。

**UIA 驗證** 是由稱為消費者介面自動化測試程式庫的 API，以及稱為 Visual **消費者介面自動化驗證** 的 GUI 介面所組成。 以下主題將說明這些情況。

> [!NOTE]
> **消費者介面自動化 Verify** 是舊版工具。 建議您改為使用 [協助工具深入](https://accessibilityinsights.io/) 解析。

## <a name="requirements"></a>規格需求

消費者介面自動化必須存在於系統上。 如需詳細資訊，請參閱 [消費者介面自動化](entry-uiauto-win32.md)的「需求」一節。

**UIA Verify** 會安裝為 Windows SDK 的整體工具組的一部分，而不是以個別下載方式來散發。 Windows SDK 包含本節中記載的所有協助工具相關工具。 [取得 Windows SDK。](https://developer.microsoft.com/) 如果您需要先前的版本， (也有從該頁面連結的 SDK 下載封存。 ) 

若要執行 **UIA 確認** 作為視覺化檢視，請在 [bin platform UIAVerify] 資料夾中找出 VisualUIAVerifyNative.exe， \\ \\ <  > \\ 然後執行它 (您通常不需要以系統管理員身分執行) 。 如需詳細資訊，請參閱 [Visual 消費者介面自動化驗證](visual-ui-automation-verify.md)。 若要使用程式庫，請參閱 [消費者介面自動化測試程式庫](ui-automation-test-library.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[協助工具事件監控程式](accessible-event-watcher.md)
</dt> <dt>

[檢查](inspect-objects.md)
</dt> <dt>

[測試控管](testing-tools.md)
</dt> <dt>

[UI 協助工具檢查程式](ui-accessibility-checker.md)
</dt> </dl>

 

 




