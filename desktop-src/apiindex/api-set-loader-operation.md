---
description: 描述 Windows 10 如何使用載入器作業中的 API 集合。
title: API 集合載入器作業
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 701409c0d8dac2c275add06d2502c8764d502aba
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "106975580"
---
# <a name="api-set-loader-operation"></a>API 集合載入器作業

[API 集會](windows-apisets.md) 依賴程式庫載入器中的作業系統支援，以有效地將模組命名空間重新導向至程式庫系結程式。 程式庫載入器會使用 [API 集合約名稱](windows-apisets.md#api-set-contract-names) ，針對裝載適當的 API 集執行的目標主機二進位檔，執行其參考的執行時間重新導向。

當載入器在執行時間遇到對 API 集的相依性時，載入器會查閱映射中的設定資料，以識別 API 集的主機二進位檔。 這項設定資料稱為 **API 集架構**。 架構會組合為 OS 的屬性，而且 API 集合和二進位檔之間的對應可能會根據指定裝置中包含的二進位檔而有所不同。 架構可讓單一二進位檔中的匯入函式在不同的裝置上正確地路由傳送，即使二進位主機的模組名稱已重新命名或在不同的 Windows 裝置上完全重構亦同。

Windows 10 支援兩種標準技術來取用和介面與 API 集合： **直接轉送** 和 **反向轉送**。

### <a name="direct-forwarding"></a>直接轉送

在此設定中，使用程式碼會直接匯入 API 集模組名稱。 這項匯入是在單一作業中解決，而且是最有效率的方法，最少的額外負荷。 就概念而言，此解析可能會指向不同 Windows 10 裝置上的不同二進位檔，如下列範例所示：

匯入的 API 集： **api-feature1-l1-1-0.dll**
-  Windows 電腦-> **feature1.dll**
-  HoloLens-> **feature1_holo.dll**
-  IoT-> **feature1_iot.dll**

因為對應會保存在自訂架構資料存放庫中，所以表示以 **.dll** 結尾的 API 集名稱不會直接參考磁片上的檔案。 API 集合名稱的 **.dll** 部分只是載入器所需的慣例。 API 集合名稱比較像是實體 DLL 檔案的別名或虛擬名稱。 這讓名稱可在整個 Windows 10 裝置的範圍內移植。

### <a name="reverse-forwarding"></a>反向轉送

雖然 API 集合名稱會為跨裝置的模組提供穩定的命名空間，但將每個二進位檔轉換成這個新系統並不一定都可行。 例如，應用程式可能已普遍使用多年，而重新編譯應用程式的二進位檔可能不可行。 此外，某些應用程式可能需要繼續在引進特定 API 集合之前建立的系統上執行。

為了滿足此層級的相容性，所有涵蓋 WIN32 API 介面子集的 Windows 10 裝置 *上都會提供* 轉寄站系統。 這些轉寄站使用在 Windows 電腦上引進的模組名稱，並利用 API 集系統來提供所有 Windows 10 裝置的相容性。

載入器作業的運作方式如下：

1.  在 Windows 電腦以外的裝置上，載入器會顯示在裝置上不存在的舊版 Windows 電腦模組名稱相依性。
2.  載入器會尋找此模組的 API 集合轉寄站，並將其載入記憶體。
3.  轉寄站具有針對所呼叫之指定函式所設定的 API 對應。
4.  載入器會為指定的裝置尋找適當的主機二進位檔。

就概念而言，對應看起來像這樣：

匯入的 DLL： **feature1.dll**
- Windows 電腦-> **feature1.dll**
- HoloLens-> **feature1.dll** 轉寄站-> **api-feature1-l1-1-0.dll**  ->  **feature1_holo.dll**
- IoT > **feature1.dll** 轉寄站-> **api-feature1-l1-1-0.dll**  ->  **feature1_iot.dll**

最終結果的功能與 [直接轉送](#direct-forwarding)相同，但它會以最大化應用程式相容性的方式來完成。

> [!NOTE]
> 反向轉送僅提供 WIN32 API 介面子集的涵蓋範圍。 它不允許以桌上出版 Windows 10 為目標的應用程式在所有 Windows 10 裝置上執行。
