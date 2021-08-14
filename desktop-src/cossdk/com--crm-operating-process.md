---
description: COM + CRM 操作進程
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: COM + CRM 操作進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d294d60429faeaad7a4d58808760ecd327bcaff252f2b71070c6605f5327ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308127"
---
# <a name="com-crm-operating-process"></a>COM + CRM 操作進程

在正常操作中，在伺服器應用程式進程中執行的應用程式元件會藉由建立 CRM 背景工作來使用 COM + CRM。 CRM 工作者會針對它所設計來執行的工作，執行特定的 COM 介面。 應用程式元件必須在交易下執行，讓 CRM 背景工作角色繼承應用程式元件的交易。 CRM 工作者一律需要交易。

為了存取 COM + CRM，CRM worker 會先取得 [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) 介面，這可讓 crm 背景工作角色將記錄寫入永久性記錄檔。 CRM 工作者會藉由建立 CRM 職員元件來取得這個介面。

接下來，CRM 工作者必須告訴 CRM 員工想要使用的 CRM 補償器的名稱。 它會藉由呼叫 [**ICrmLogControl：： RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) 方法來執行此動作。 呼叫這個方法之後，crm 基礎結構會在交易完成時建立 CRM 補償器。

當 CRM 工作者註冊其 CRM 補償器之後，它就可以使用 [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)將記錄寫入 crm 記錄檔。 CRM 工作者必須 *事先撰寫*;也就是說，它必須在執行動作之後立即發生損毀的記錄檔中，將記錄寫入描述動作的記錄。 如果沒有這些預先寫入的記錄檔記錄，就無法更正動作。

此外，事先撰寫表示 CRM 補償器（也就是在復原時接收記錄檔記錄的元件）必須處理記錄檔記錄已寫入但動作實際上不發生的情況。 CRM 補償器的動作必須為 *等冪*;也就是說，它們應該能夠執行一次以上，但應該會產生相同的結果。 例如，將帳戶餘額設定為 $100 的值是等冪動作;將 $100 新增至帳戶餘額不是。

[**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)介面提供下列兩個撰寫記錄檔記錄的方法：

-   [**WriteLogRecordVariants**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) 可用來撰寫以 variant 集合形式建立的結構化記錄。 這主要是在 Microsoft Visual Basic 中開發 Crm 時使用。
-   [**WriteLogRecord**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) 可用來將非結構化記錄檔記錄寫入為位元組的 blob。 這主要是在 Microsoft Visual C++ 開發 Crm 時使用。 因為 C 中的記錄結構通常是由一組可能分散在記憶體中的標頭和欄位所組成，所以 **WriteLogRecord** 方法會執行收集功能，以減少資料的複製。

> [!Note]  
> 您不應該在記錄檔記錄中的資料結構內輸入使用者指標類型。 在復原階段中，指標已不再有效，因為 CRM 補償器在不同的進程中執行，而非寫入記錄檔記錄的 CRM worker。 在記錄檔記錄中包含指標類型可能會導致應用程式在復原期間損毀或損毀。

 

這兩個寫入方法會將記錄檔記錄寫入磁片，但不保證記錄的持久性。 雖然允許在強制磁片之前累積延遲寫入，才能提升效能，但您可以使用 [**ICrmLogControl：： ForceLog**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) 方法，以確保 CRM 完成的所有寫入都在磁片上是永久性的，這對失敗復原很重要。

當 CRM 工作者完成其動作並完成寫入記錄並強制執行記錄時，它必須發行 [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)。 當交易完成時 (通常是因為呼叫 [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 或 [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)) 的應用程式元件所造成，crm 基礎結構會建立 crm 補償器元件，它會執行 [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) 介面或 [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) 介面。 這些介面可用來將非結構化 (Visual C++) 或結構化 (Visual Basic) 記錄傳遞至 CRM 補償器，以及交易結果通知。

CRM 補償器會先收到交易完成的準備階段通知，並且可以將「是」或「否」投票給準備要求。 如果 CRM 補償器投票否，則不會收到任何進一步的中止通知。 如果它對準備要求投票為 yes，則會接收認可或中止通知。 在用戶端中止的情況下，不會收到任何準備通知，只會中止通知。 CRM 補償器必須準備好處理所有這些情況，而且也必須處理 CRM 背景工作未成功寫入任何記錄檔記錄的情況。 CRM 補償器不能假設相同的 CRM 補償器實例會同時收到第1階段 (準備) 和第2階段 (認可或中止) 通知，因為這些可能會被覆原中斷。

通常，CRM 補償器會使用中止通知來反轉 CRM 背景工作所執行的動作。 如果需要反轉動作，CRM 背景工作可能會讓某些狀態維持可用狀態。 該狀態可能會完全包含在記錄檔記錄中，如果沒有，則 CRM 補償器必須在交易認可時清除該狀態。 這是 CRM 補償器收到認可通知的原因。 CRM 補償器不會在 DTC 交易下執行。

CRM 補償器可以在有需要時使用 [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)來記錄新的記錄，其會在建立時收到。 CRM 工作者和 CRM 補償器也可能會忘記最後寫入的記錄檔記錄，這可能是避免不必要的復原所需的記錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[COM + CRM 啟動和復原](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



