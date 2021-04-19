---
description: 下列程式碼範例示範如何建立呼叫物件、探索與呼叫相關聯的資料流程、選取和建立適當的終端機、選取資料流程上的終端機，以及完成連接。
ms.assetid: 49815b18-a8ea-46e0-b2a4-3d7a82e727b0
title: 撥打電話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc22ebde34e65c9acc8e6c7dd81944b06804935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978879"
---
# <a name="make-a-call"></a>撥打電話

下列程式碼範例示範如何建立呼叫物件、探索與呼叫相關聯的資料流程、選取和建立適當的終端機、選取資料流程上的終端機，以及完成連接。

使用此程式碼範例之前，您必須先在 [初始化 TAPI](initialize-tapi.md) 中執行作業，然後 [選取位址](select-an-address.md)。

此外，您必須在呼叫 [**ITAddress：： CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)之後，執行 [選取終端](select-a-terminal.md)機中說明的作業。

> [!Note]  
> 此範例沒有適用于實際執行程式碼的錯誤檢查和發行。

 

``` syntax
// Specify the destination address.
//
// szAddressToCall and 
// dwAddressType have been
// retrieved from a user interface.
ITBasicCallControl * pBasicCall
bstrAddressToCall = SysAllocString( szAddressToCall );
// If ( bstrAddressToCall == NULL ) process the error here. 

HRESULT hr = pAddress->CreateCall(
    bstrAddressToCall,
    dwAddressType,
    &pBasicCall
 );
// If ( hr != S_OK ) process the error here. 

SysFreeString(bstrAddressToCall);

// Create the required terminals for this call.
{
    // See the Select a Terminal code example.
}

// Make the connection.
pBasicCall->Connect( TRUE );
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITBasicCallControl：： Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



