---
description: 安全通道通訊協定引擎會在安全的程式中，以及在應用程式進程中傳遞大量加密/訊息的方式，執行信號交換和驗證。
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: 跨越進程界限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970589"
---
# <a name="crossing-process-boundaries"></a>跨越進程界限

安全 [*通道通訊協定*](../secgloss/s-gly.md) 引擎會在安全的程式中，以及在應用程式進程中傳遞大量加密/訊息的 [*方式，執行*](../secgloss/p-gly.md) 信號交換和驗證。 這表示 [*大量加密金鑰*](../secgloss/b-gly.md) 和 [*MAC*](../secgloss/m-gly.md) 金鑰必須從一個進程複製到另一個進程。 若要將金鑰從某個進程複製到另一個進程，請使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) 和 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 功能，如下所示：

1.  安全進程會使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)將每個金鑰匯出到 [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) ，然後使用 [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey)來終結金鑰。 請注意，如果金鑰儲存在硬體中，則 CSP 必須辨識這一點，且不能嘗試終結金鑰。
2.  安全進程會以超出本檔範圍的方式，將 OPAQUEKEYBLOBs 傳遞至應用程式進程。
3.  應用程式進程會使用 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)，將每個 OPAQUEKEYBLOB 匯入回 CSP。 此時，金鑰必須與匯出時的 [*狀態*](../secgloss/s-gly.md) 完全相同。

 

 
