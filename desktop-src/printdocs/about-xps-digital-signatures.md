---
description: 本節提供 XPS 數位簽章 API 的總覽。
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: 關於 XPS 數位簽章 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba2bad4ef10d8800e9a4cb59289fccb75cc2d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115485"
---
# <a name="about-xps-digital-signature-api"></a>關於 XPS 數位簽章 API

XPS 檔可以有數位簽章，讓使用者可以簽署檔、確認簽署者的身分識別，並指出 XPS 檔在簽署之後是否已經變更。 原生 Windows 應用程式可以使用 XPS 數位簽章 API 的介面來執行 XPS 檔的數位簽章作業。 本節提供 XPS 數位簽章 API 的總覽。

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)介面會管理 XPS 檔的數位簽章作業。 應用程式必須先呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立 **IXpsSignatureManager** ，然後呼叫 [**IXpsSignatureManager：： LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) 或 [**IXpsSignatureManager：： LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) 來載入 xps 檔，應用程式才能存取 xps 檔的數位簽章。 如需此初始化程式的詳細資訊，請參閱初始化簽章 [管理員](initialize-the-signature-manager.md)。

將 XPS 檔載入 [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) 介面之後，應用程式就可以存取檔的數位簽章和數位簽章要求。 您可以使用簽章管理員的 [**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)介面中的 [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)介面來存取數位簽章。 應用程式也可以新增和移除集合中的 **IXpsSignature** 介面。 您可以使用在 [**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)介面中收集的 [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)來存取簽章要求。 **IXpsSignatureRequestCollection** 是 [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)介面的一部分，會在簽章管理員的 [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)中收集。

應用程式可以使用簽章管理員的 [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) 來存取和設定數位簽章選項。

如需如何存取 XPS 檔數位簽章的範例，請參閱常見的 [數位簽章程式設計](basic-digital-signature-programming-tasks.md)工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 XPS 數位簽章 API](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[XPS 數位簽章 API 參考](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[包裝](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[標準 ECMA-376、Office Open XML 檔案格式](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
