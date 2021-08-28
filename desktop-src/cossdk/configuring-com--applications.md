---
description: COM + 應用程式基本上是一種宣告式的結構，可讓您設定任何數目的萬用群組件。 例如，您可以使用一般安全性原則來設定應用程式中的元件。
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: 設定 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d6c8caa8dc4ca949a71d9a6b56fd6eae95d415
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465995"
---
# <a name="configuring-com-applications"></a>設定 COM + 應用程式

COM + 應用程式基本上是一種宣告式的結構，可讓您設定任何數目的萬用群組件。 例如，您可以使用一般安全性原則來設定應用程式中的元件。

在 COM + 應用程式的開發程式中，設定是不可或缺的一部分。 您如何設定應用程式，將決定 COM + 如何為其提供服務，以及在執行時如何運作。

您可以使用 [元件服務] 系統管理工具或可編寫腳本的管理物件和介面（提供管理工具的基礎功能）來設定 COM + 應用程式。 如需執行腳本管理的詳細資訊，請參閱 [自動化 COM + 管理](automating-com--administration.md)。

您可以在 COM + 應用程式內的下列層級設定元素：

-   [應用層級設定](#application-level-settings)
-   [元件層級 (類別層級) 設定](#component-level-class-level-settings)
-   [介面層級設定](#interface-level-setting)
-   [方法層級設定](#method-level-setting)
-   [相關主題](#related-topics)

您將元件安裝到應用程式的方式，可能會影響您如何進行設定。 您應該一律將元件安裝至 COM + 應用程式 (而不是將它們匯入) 。 安裝元件會在 COM + 類別註冊資料庫中完整註冊它們，以及介面和類型程式庫 (RegDB) ，讓您可以進行設定。

## <a name="application-level-settings"></a>Application-Level 設定



| 屬性                                                                                        | 描述                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [啟動](context-activation.md)<br/>                                                  | 指定應用程式類型： [伺服器應用程式] 或 [程式庫應用程式]。<br/>                                                                                                            |
| [啟用存取檢查](enabling-access-checks-for-an-application.md)<br/>               | 開啟和關閉安全性檢查。<br/>                                                                                                                                                      |
| [安全性層級](setting-a-security-level-for-access-checks.md)<br/>                      | 指定將在進程層級執行存取檢查， (從角色) 或同時在進程和元件層級產生的存取檢查層級 (完整的角色型安全性) 。<br/> |
| [驗證等級](setting-an-authentication-level-for-a-server-application.md)<br/>  | 設定用於呼叫應用程式的驗證層級。<br/>                                                                                                                        |
| [模擬等級](setting-an-impersonation-level.md)<br/>                             | 設定呼叫其他應用程式時所使用的模擬等級。<br/>                                                                                                                        |
| [排隊](creating-queuable-components.md)<br/>                                           | 指定應用程式元件將使用佇列服務。<br/>                                                                                                                         |
| [啟用 CRM](configuring-com--crm-components.md)<br/>                                     | 啟用補償資源管理員的使用。<br/>                                                                                                                                           |
| [以服務形式執行應用程式](com--applications-running-as-service-applications.md)<br/> | 將 COM + 伺服器應用程式設定和實作為 NT 服務。<br/>                                                                                                                    |
| [COM + SOAP 服務](com--soap-service.md)<br/>                                            | 將 COM + 應用程式公開為 XML web service。<br/>                                                                                                                                        |
| [應用程式共用](com--application-pooling.md)<br/>                                   | 為單一執行緒進程新增擴充性，並與 COM + 應用程式回收服務整合。<br/>                                                                               |
| [應用程式回收](com--application-recycling.md)<br/>                               | 藉由正常關閉與應用程式相關聯的進程並重新啟動，來提高應用程式穩定性。<br/>                                                                  |
| [進程傾印](what-s-new-in-com--1-5.md)<br/>                                         | 傾印整個進程的狀態，而不終止它，以供進行調試。<br/>                                                                                                      |
| 伺服器進程關機<br/>                                                               | 在指定的閒置期限之後關閉進程。<br/>                                                                                                                                      |
| 權限<br/>                                                                           | 停用設定的變更，包括刪除。<br/>                                                                                                                          |
| 安全性身分識別<br/>                                                                     | 指定應用程式執行時所用的身分識別。<br/>                                                                                                                                 |
| 在偵錯工具中啟動<br/>                                                                    | 指定將在偵錯工具中啟動應用程式，並使用使用者指定的命令列設定。<br/>                                                                                |
| 啟用 3GB 支援<br/>                                                                    | 啟用擴充進程記憶體位址空間的使用。<br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a>Component-Level (類別層級) 設定




| 屬性 | 描述 | 
|-----------|-------------|
| <a href="configuring-transactions.md">交易</a><br /> | 設定停用、不支援、支援、必要或需要新的自動交易需求。<br /> | 
| <a href="setting-the-synchronization-attribute.md">同步處理</a><br /> | 設定停用、不支援、支援、必要或需要新的同步處理需求。<br /> | 
| <a href="enabling-jit-activation-for-a-component.md">JIT 啟用</a><br /> | 啟用即時啟用。<br /> | 
| <a href="configuring-a-component-to-be-pooled.md">物件集區</a><br /> | 啟用物件共用。 最小和最大集區大小和物件超時值都是可設定的。<br /> | 
| <a href="specifying-an-object-constructor-string-for-a-component.md">物件結構</a><br /> | 使用系統管理指定的函式字串來啟用參數化物件結構。 <br /><blockquote>[!Note]<br />不應使用此函式字串來儲存安全性機密資訊。</blockquote><br /> | 
| <a href="enabling-access-checks-at-the-component-level.md">元件層級存取檢查</a><br /> | 開啟或關閉元件層級以角色為基礎的安全性檢查。<br /> | 
| <a href="assigning-roles-to-components--interfaces--or-methods.md">宣告式角色指派</a><br /> | 啟用將角色明確指派給元件。<br /> | 
| <a href="persistent-client-side-failures.md">佇列例外狀況類別</a><br /> | 表示處理用戶端失敗的例外狀況類別。<br /> | 
| <a href="com--instrumentation-concepts.md">檢測事件和統計資料</a><br /> | 啟用詳細的系統事件和物件統計資料包告。<br /> | 
| <a href="context-activation.md">啟用內容</a><br /> | 啟用在呼叫端的內容或預設內容中強制啟用物件。<br /> | 
| <a href="what-s-new-in-com--1-5.md">建立私用元件</a><br /> | 將元件標示為私用應用程式。 私用元件只能由相同應用程式中的其他元件來查看和啟用。<br /> | 




 

## <a name="interface-level-setting"></a>Interface-Level 設定



| 屬性                                                                                           | 描述                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [已排入佇列](creating-queuable-components.md)<br/>                                               | 表示 IDL 中定義的 queuable 介面。<br/>                                                                       |
| [宣告式角色指派](assigning-roles-to-components--interfaces--or-methods.md)<br/> | 可以明確地將角色指派給介面，以及從元件層級隱含繼承角色。<br/> |



 

## <a name="method-level-setting"></a>Method-Level 設定



| 屬性                                                                                           | 描述                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [自動完成](enabling-auto-done-for-a-method.md)<br/>                                         | 自動停用方法傳回的物件和交易中的投票。<br/>                                                       |
| [宣告式角色指派](assigning-roles-to-components--interfaces--or-methods.md)<br/> | 可以明確地將角色指派給方法，以及從介面和元件層級隱含繼承角色。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自動化 COM + 管理](automating-com--administration.md)
</dt> <dt>

[建立 COM + 應用程式](creating-com--applications.md)
</dt> <dt>

[部署 COM + 應用程式](deploying-com--applications.md)
</dt> </dl>

 

 




