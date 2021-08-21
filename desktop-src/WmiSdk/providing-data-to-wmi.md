---
description: wmi 可透過 wmi 提供者取得 Windows 可管理物件的相關資料。
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: 將資料提供給 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22fbff46959c001f589587f21b8b2b50ab5c5187d387338f407bf45e3e1a29d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316572"
---
# <a name="providing-data-to-wmi"></a>將資料提供給 WMI

wmi 可透過 wmi [*提供者*](gloss-p.md)取得 Windows 可管理物件的相關資料。 提供者會從系統元件（例如，處理常式）或已檢測的應用程式（例如 SNMP 或 IIS）抓取資料，並透過 WMI 將該資料傳遞至管理應用程式。 例如，當應用程式或腳本使用 WMI [**Win32 \_ process**](/windows/desktop/CIMWin32Prov/win32-process) 類別來要求處理資訊時，會透過預先安裝的提供者動態取得資料。

本主題將討論下列各節：

-   [為可管理的物件建立模型](#creating-a-model-for-a-manageable-object)
-   [針對可管理的物件執行模型](#implementing-a-model-for-a-manageable-object)
-   [判斷要執行的提供者類型](#determining-a-provider-type-to-implement)
-   [判斷提供者的裝載 (實) 模型](#determining-a-hosting-implementation-model-for-a-provider)
-   [執行提供者](#implementing-a-provider)
-   [向 WMI 和系統註冊提供者](#registering-a-provider-with-wmi-and-the-system)
-   [測試提供者](#testing-a-provider)
-   [相關主題](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a>為可管理的物件建立模型

開發提供者之前，請先建立資料模型來代表可透過 WMI 公開的可管理物件。 您可以規劃提供者將公開的資料物件。 例如，如果您打算管理桌面背景的螢幕解析度，就必須決定如何在 [*受控物件格式 (MOF)*](gloss-m.md) 檔中建立桌面模型。

若要建立有用的模型：

-   判斷真實世界的案例，並為客戶可能想要讀取和更新的資訊建立模型 (例如，變更每個可管理物件的背景影像) 。 這些是您的類別屬性。
-   判斷客戶可能想要對每個可管理的物件執行何種動作。 這些都是您的方法。

## <a name="implementing-a-model-for-a-manageable-object"></a>針對可管理的物件執行模型

若要針對可管理的物件執行模型，請建立一個 MOF 檔案，其中包含代表每個物件的 WMI 類別。 如需建立 MOF 檔案以定義 WMI 類別的詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。 註冊提供者及其類別通常會包含在 MOF 檔案中，雖然您可以使用 [COM API](com-api-for-wmi.md) 來建立類別和方法。 如需詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。

> [!Note]  
> 若要確保在 WMI 失敗並重新啟動時，managed 物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請使用 [*受控物件格式 (MOF)*](gloss-m.md)檔中的 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器指令。

 

建立 MOF 檔案之後，請使用 [**Mofcomp.exe**](mofcomp.md) 工具進行編譯。 這會通知您 MOF 檔案中的錯誤，並將 MOF 檔案中定義的 WMI 類別新增至 [*wmi 儲存*](gloss-w.md) 機制，讓提供者可以使用此類別。

## <a name="determining-a-provider-type-to-implement"></a>判斷要執行的提供者類型

WMI 支援特定數目的提供者類型，可決定提供者所支援之資訊和作業的本質。

提供者類型為：

-   [*執行個體提供者*](gloss-i.md)
-   [*方法提供者*](gloss-m.md)
-   [*屬性提供者*](gloss-p.md)
-   類別提供者
-   [*事件提供者*](gloss-e.md)
-   [*事件取用者提供者*](gloss-e.md)
-   [*關聯提供者*](gloss-a.md)

大部分的提供者都是執行個體提供者和方法提供者。 執行個體提供者是最常見的提供者，它會提供指定類別的實例。 方法提供者會執行一個或多個類別的方法。 如需提供者類型的詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>判斷提供者的裝載 (實) 模型

WMI 提供者是實作為 COM 物件的二進位檔。 這表示每個提供者都有一個 DLL 檔案，可在特定進程和安全性內容中執行。 這是 WMI 所謂的 [*裝載模型*](gloss-h.md)。 WMI 提供各種不同的方式來主控提供者，但最常見的方法是使用結合的提供者模型 (在 NetworkServiceHost 安全性內容中) 的 WMI 進程下執行。 WMI 提供者可分類為結合或 [*分離*](gloss-d.md)。

「結合」或「分離」提供者會根據提供的 WMI （WMIPRVSE.EXE 程式），決定執行提供者所依據的主機進程。 最佳做法是判斷提供者公開的管理資料，以及它所依賴的 API 或應用程式是否一律可在系統中使用。 如果提供者所依賴的 API 或應用程式永遠可用 (在系統) 上執行，則提供者應該是結合的提供者，如果不是，則必須是低耦合提供者。 如需裝載模型的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

如需有關建立結合提供者的詳細資訊，請參閱 [撰寫提供者以將資料提供給 WMI](supplying-data-to-wmi-by-writing-a-provider.md)，以及如需在應用程式中納入低耦合提供者的詳細資訊，請參閱 [在應用程式中併入提供者](incorporating-a-provider-in-an-application.md)。

結合的提供者可以描述為同進程 (內建) 或跨進程的 (跨進程) 。 當結合的提供者是內建提供者時，它會在共用 WMIPRVSE.EXE WMI 裝載進程下執行，並實作為 COM 的內部進程伺服器 (.dll) 。 當提供者是跨進程提供者時，它會在要求用戶端或事件時由 WMI 啟動，但會以分開進程的形式執行，並實作為可執行檔 (.exe) 。

## <a name="implementing-a-provider"></a>執行提供者

您可以透過下列方式實作為提供者：

-   使用 Visual Studio 中的 ATL Wizard。

    ATL Wizard 會產生可執行結合提供者的提供者程式碼。 當您使用 ATL Wizard 時，可以指定您想要建立同進程 (.dll) 或非進程 (.exe) 提供者執行時間模型。

-   定義要包含提供者的 COM 物件。

    提供者程式碼是以 c + + 撰寫。 如需詳細資訊，請參閱 [撰寫提供者以將資料提供給 WMI](supplying-data-to-wmi-by-writing-a-provider.md)。

-   使用 .NET Framework [**中的類別**](/previous-versions//hh872326(v=vs.85))，利用 managed 程式碼來建立提供者。 不再支援 (**系統. Management. Instrumentation** 命名空間。 ) 

    此進程會建立低耦合提供者。

## <a name="registering-a-provider-with-wmi-and-the-system"></a>向 WMI 和系統註冊提供者

使用來自取用者的提供者之前，請務必先向 WMI 系統和 Windows COM 子系統進行註冊。

MOF 檔案可以包含相同類別的多個提供者類型。 相同的提供者名稱會註冊為，例如實例或方法提供者。 如需詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。

## <a name="testing-a-provider"></a>測試提供者

註冊提供者程式碼時，請務必使用不同取用者的提供者來適當測試提供者 (例如，腳本、.NET managed 程式碼和 c + + 取用者) 。

執行下列工作以測試您的提供者：

-   藉由追蹤 [**MSFT \_ 的 wmiprovider \_ OperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) 事件通知，確定您的提供者已正確載入。 這些事件會通知您有任何提供者載入失敗。 其他可能會有説明的疑難排解類別是 [**win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) 和 [**win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)。 如需疑難排解提供者的詳細資訊，請參閱 [偵錯工具](debugging-providers.md) 和 [提供者設定和疑難排解類別](provider-configuration-and-troubleshooting-classes.md)。
-   如果提供者是實例或方法提供者，請務必逐一測試每一項提供者功能，以避免混淆您的程式碼邏輯。
-   若為執行個體提供者，請建立用戶端應用程式或腳本，以叫用提供者的每個介面 (列舉、get、put 和 delete) 。 即使提供者不應執行任何作業，它也應該會傳回「不支援」的訊息。 您可以找到已在 [WMI 傳回碼](wmi-return-codes.md)中定義的傳回值。
-   為了確保所需的安全性內容如預期運作，請從非管理員的安全性內容叫用提供者支援的作業。 提供者必須支援模擬。 如果缺少正確安全性認證的使用者嘗試更新資料，或執行執行方法的作業，則您的提供者應該使用適當的錯誤訊息來拒絕存取。
-   如需提供者安全性的詳細資訊，請參閱 [保護您的提供者](securing-your-provider.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> <dt>

[提供者裝載和安全性](provider-hosting-and-security.md)
</dt> <dt>

[藉由撰寫提供者，將資料提供給 WMI](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[將提供者併入應用程式中](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[註冊提供者](registering-a-provider.md)
</dt> <dt>

[疑難排解 WMI 用戶端應用程式](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[保護您的提供者](securing-your-provider.md)
</dt> <dt>

[在64位平臺上取得和提供資料](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
