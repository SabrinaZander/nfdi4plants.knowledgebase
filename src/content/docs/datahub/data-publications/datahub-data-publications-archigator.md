---
title: Submitting ARCs with ARChigator
lastUpdated: 2024-07-10
authors:
  - kevin-schneider
---

:::note
All CQC pipelines are opt-in starting from July 10, 2024. If you used the DataHUB publication service before, head [here](/nfdi4plants.knowledgebase/arc-validation/validation-packages) to learn how to opt-in.
:::

ARChigator is a tool for submitting ARCs hosted on DataHUB for publication in the [ARChive](https://archive.nfdi4plants.org/communities/dataplant).

## Start the publication process

To start the publication process, first make sure to install the [invenio validation package](https://avpr.nfdi4plants.org/package/invenio). On the commit click on the _invenio badge_ on the ARC homepage. Make sure that the validation against the invenio package  passes (indicated by a green badge), otherwise you will not be able to proceed to the next steps.

## Review record metadata

After clicking the badge, you will be redirected to the ARChigator page, where you can review the metadata of the record that will be created in the ARChive. Note that you can only proceed to this page if you are logged in to DataHUB.

![](@images/data-publications/archigator-metadata-review.png)

- **(4)**: The source of your ARC
- **(5)**: Selected investigation metadata from the ARC that will also be shown in the publication record
- **(6)**: Author metadata from the ARC that will also be shown in the publication record. Note that author details are blacked out here for privacy reasons.

Once you double-checked the metadata, you can proceed to submitting the ARC.

## Submit the ARC


![](@images/data-publications/archigator-submit.png)

- **(7)**: Name and image of the ARC. The `Ready` badge signifies that this ARC is eligible for publication (it has passed the CQC pipeline **(1)**). Note that you are stopped from publishing here at latest if the CQC pipeline fails.
- **(8)**: You cannot publish an ARC that you do not have access control for on the DataHUB instance it is hosted on.
- **(9)**: You can only publish an ARC if you agree to the terms of use of the ARChive and made sure to include all authors.
- **(10)**: Clicking on the _publish button_ will submit the ARC to the ARChive.

After clicking on the _publish button_ (**10**), your ARC is officially in Request For Publication (**RFP**) stage. You will receive a confirmation mail with a link to the publication status page of your ARC.

## Publication status

Once you clicked on the _publish button_ (**10**), you will be redirected to the submission ticket, and receive a confirmation mail. For more information on tracking the publication progress, refer to this [guide](/nfdi4plants.knowledgebase/datahub/data-publications/datahub-data-publications-status).
