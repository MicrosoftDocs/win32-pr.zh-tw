---
description: 說明如何建立 CALG \_ SSL3 \_ SHAMD5 hash。
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: 建立 CALG_SSL3_SHAMD5 雜湊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996811"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a>建立 CALG \_ SSL3 \_ SHAMD5 雜湊

**若要建立 CALG \_ SSL3 \_ SHAMD5 雜湊**

1.  使用標準 CryptoAPI 方法，同時建立 MD5 和目標資料的 [*SHA*](../secgloss/s-gly.md) [*雜湊*](../secgloss/h-gly.md) 。
2.  串連兩個雜湊，最左邊的 MD5 值和 SHA 值。 這會產生36個位元組值 (16 個位元組 + 20 個位元組) 。
3.  藉由呼叫 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with CALG SSL3 SHAMD5 傳入 Algid 參數，取得 [*雜湊物件*](../secgloss/h-gly.md)的控制碼 \_ \_ 。 
4.  使用 [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam)的呼叫來設定雜湊值。 串連的雜湊值會在 >pbdata 參數中當作 **位元組** 傳遞 \* ，且 \_ 必須在 *dwParam* 參數中傳遞 HP HASHVAL 值。 在步驟3中使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)所傳回的控制碼呼叫 [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)將會失敗。
5.  呼叫 [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) 以產生簽章。
6.  呼叫 [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) 終結雜湊物件。

 

 
