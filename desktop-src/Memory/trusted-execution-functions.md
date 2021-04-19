---
description: 使用用來建立信任執行環境的記憶體保護區時，會使用下列函數：
ms.assetid: DF6CDEE1-CAAA-429C-9939-DDC844302027
title: 信任的執行函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b1bd2411d0448346f0a8afcca870c26b4a61ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972074"
---
# <a name="trusted-execution-functions"></a>信任的執行函數

使用用來建立信任執行環境的記憶體保護區時，會使用下列函數：

## <a name="in-this-section"></a>本節內容



| 主題                                                                               | 描述                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-callenclave)<br/>                                       | 呼叫記憶體保護區中的函式。 <br/>                                                                                                                                                                                |
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)<br/>                                   | 建立新的未初始化記憶體保護區。 記憶體保護區是程式碼的隔離區域，以及應用程式位址空間內的資料。 只有在記憶體保護區中執行的程式碼可以存取相同記憶體保護區內的資料。<br/> |
| [**DeleteEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-deleteenclave)<br/>                                   | 刪除指定的記憶體保護區。<br/>                                                                                                                                                                                      |
| [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>       | 取得描述目前記憶體保護區的記憶體保護區證明報表，並由負責記憶體保護區型別的授權單位簽署。 <br/>                                                              |
| [**EnclaveGetEnclaveInformation**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation)<br/>     | 取得目前執行之記憶體保護區的相關資訊。<br/>                                                                                                                                                             |
| [**EnclaveSealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata)<br/>                               | 從 unencypted 資料產生加密的二進位大型物件 (blob) 。<br/>                                                                                                                                             |
| [**EnclaveUnsealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveunsealdata)<br/>                           | 將加密的二進位大型物件解密 (blob) 。<br/>                                                                                                                                                                   |
| [**EnclaveVerifyAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveverifyattestationreport)<br/> | 驗證在目前系統上產生的證明報告。 <br/>                                                                                                                                           |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave)<br/>                           | 初始化您建立並載入資料的記憶體保護區。<br/>                                                                                                                                                       |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported)<br/>                 | 抓取是否支援指定的記憶體保護區類型。<br/>                                                                                                                                                       |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)<br/>                               | 將資料載入您藉由呼叫 [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)所建立的未初始化記憶體保護區。<br/>                                                                                                        |
| [**LoadEnclaveImage**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-loadenclaveimagew)<br/>                             | 將影像及其所有匯入載入記憶體保護區中。<br/>                                                                                                                                                              |
| [**TerminateEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-terminateenclave)<br/>                             | 結束在記憶體保護區中執行的執行緒執行。<br/>                                                                                                                                               |



 

 

 




