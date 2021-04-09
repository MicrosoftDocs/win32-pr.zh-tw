---
title: Active Directory 服務介面
description: Active Directory 的服務介面簡介，並連結至不同的指南。
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- 'Active Directory 服務介面 (查看 ADSI) '
- ADSI ADSI、起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024091"
---
# <a name="active-directory-service-interfaces"></a>Active Directory 服務介面

## <a name="purpose"></a>目的

Active Directory 服務介面 (ADSI) 是一組 COM 介面，可用來從不同的網路提供者存取目錄服務的功能。 ADSI 用於分散式運算環境中，以呈現一組用於管理網路資源的目錄服務介面。 系統管理員和開發人員可以使用 ADSI 服務來列舉和管理目錄服務中的資源，不論哪一個網路環境包含資源。

ADSI 可啟用一般管理工作，例如新增使用者、管理印表機，以及在分散式運算環境中尋找資源。

> [!Note]  
> 下列檔適用于電腦程式設計人員。 如果您是嘗試偵測列印錯誤或家用網路問題的使用者，請參閱 [Microsoft 社區論壇](https://answers.microsoft.com)。

 

## <a name="where-applicable"></a>適用時

網路系統管理員可以使用 ADSI 來自動化一般工作，例如新增使用者和群組、管理印表機，以及設定網路資源的許可權。

獨立軟體廠商和使用者開發人員可以使用 ADSI 來「目錄啟用」其產品和應用程式。 服務可以在目錄中發佈自己，用戶端可以使用目錄來尋找服務，而且兩者都可以使用目錄來尋找和操作其他感興趣的物件。 由於 Active Directory 服務介面與基礎目錄服務 (的) 無關，因此可支援目錄的產品和應用程式在多個網路和目錄環境中都能順利運作。

## <a name="developer-audience"></a>開發人員對象

您可以撰寫許多語言的 ADSI 用戶端應用程式。 針對大部分的系統管理工作，ADSI 定義了可從與 Automation 相容的語言（例如 Microsoft Visual Basic、Microsoft Visual Basic Scripting Edition (VBScript) 和 JAVA）存取的介面和物件，以提供更高效能和效率的語言，例如 C 和 c + +。 在 COM 程式設計中，良好的基礎適用于 ADSI 程式設計人員。

## <a name="run-time-requirements"></a>執行階段需求求

Active Directory 在 Windows Server 網域控制站上執行。 不過，您可以在 Windows 上撰寫和執行使用 ADSI 的用戶端應用程式。 此外，開發人員也需要平臺軟體發展工具組 (SDK) ，也可在 MSDN 網站上取得。 若要調查 Active Directory 的內容，請使用 Active Directory 消費者和電腦 MMC 嵌入式管理單元。 此嵌入式管理單元取代了舊版 Windows 所提供的 Adsvw 工具。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[關於 ADSI](about-adsi.md)
</dt> <dd>

ADSI 的一般資訊。

</dd> <dt>

[使用 ADSI](using-adsi.md)
</dt> <dd>

使用 ADSI 的程式設計師指南。

</dd> <dt>

[ADSI 快速入門教學課程](adsi-quick-start-tutorials.md)
</dt> <dd>

使用 ADSI 搭配 Automation 來管理目錄。

</dd> <dt>

[ADSI 參考](adsi-reference.md)
</dt> <dd>

ADSI 介面和方法的檔。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件物件模型](../com/the-component-object-model.md)
</dt> <dt>

[COM 用戶端和伺服器](../com/com-clients-and-servers.md)
</dt> <dt>

[Active Directory Domain Services](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 