# Electrostatic Discharge (ESD) Control for Lab and Factory Engineers and Managers — Learner Guide

**Course code:** TGS-2024051412 · **TSC:** Electrostatic Discharge Control (ELE-OPR-4002-1.1) · **Version:** v3.0 (19 August 2026)

> Detailed procedures appear here and in the individual activity folders. The PowerPoint remains concept-led.

## Learning outcomes

- LO1: Apply control measures to manage ESD generation based on ESD principles.
- LO2: Evaluate and recommend actions to improve ESD control effectiveness in accordance with ESD standards.

## Source and standards note

This guide preserves useful coverage and all embedded pictures from the legacy v2 deck, then deepens the content using the supplied sources. For exact acceptance limits, test methods and programme requirements, the organisation’s current controlled copies of the applicable standards, customer requirements and procedures govern.

## Module 1: Basics of ESD

**Mapping:** K1 · A1  
Charge generation · discharge paths · HBM/MM/CDM · failure modes · business impact

### ESD: an invisible reliability hazard

- A sudden charge transfer can damage a device without a visible spark or a felt shock.
- Treat every unprotected ESDS item as vulnerable throughout handling, test, storage and service.

> **Decision takeaway:** Human sensation is a poor detector of device risk.

*Source alignment: ESDA Fundamentals Part 1.*

### The charge–field–discharge chain

- Contact and separation create charge
- Charge remains on isolated conductors or insulators
- An electric field polarises nearby objects
- A conductive path forms
- Fast current damages a vulnerable device

*Source alignment: ESDA Fundamentals Part 1.*

### Triboelectric charging

- **Material pair:** Different electron affinities drive polarity and magnitude.
- **Contact area:** More intimate contact can transfer more charge.
- **Separation:** Speed and force affect charge generation.
- **Environment:** Humidity and contamination change surface leakage.

*Source alignment: ESDA Fundamentals Part 1.*

### Conductors, dissipative materials and insulators

- Conductors redistribute charge quickly and can be grounded.
- Dissipative materials move charge in a controlled manner.
- Insulators retain localised charge and cannot be neutralised by grounding alone.
- Low-charging, dissipative and shielding are different material functions.

> **Decision takeaway:** Select material by required function—not by colour or marketing label.

*Source alignment: ESDA Fundamentals Part 1.*

### Isolated conductors are still hazardous

- A metal tool, trolley or fixture can remain charged when it has no verified path to ground.
- Bonding removes potential differences; grounding provides a controlled reference path.

> **Decision takeaway:** Conductive does not automatically mean safe.

*Source alignment: ESDA Fundamentals Part 1.*

### Electrostatic induction and polarisation

- Charged object approaches
- Field redistributes charge in nearby conductor
- Temporary ground connection permits charge flow
- Ground is removed
- Object retains a net charge after the field leaves

> **Decision takeaway:** No physical rubbing is required for field-induced charging.

*Source alignment: ESDA Fundamentals Part 1.*

### Contact discharge versus air discharge

- Contact discharge: differently charged objects touch and charge transfers directly.
- Waveform depends on the source, path impedance and contact geometry.
- Air discharge: a strong field ionises an air gap before contact.
- Visible sparks represent only a subset of damaging ESD events.

*Source alignment: Analog Devices ESD glossary.*

### What controls discharge severity?

- **Voltage difference:** Stored potential is one risk indicator, not the whole event.
- **Capacitance:** More stored charge can raise available energy.
- **Path impedance:** Resistance and inductance shape peak current and rise time.
- **Device sensitivity:** Pins, package and internal structures determine failure threshold.

*Source alignment: ESDA Fundamentals Part 1.*

### Human Body Model (HBM)

- Represents a charged person discharging through a device pin.
- Useful for component qualification and handling robustness.
- A laboratory model—not a prediction of every factory event.
- Use supplier sensitivity data and the applicable controlled test method.

*Source alignment: Analog Devices ESD glossary.*

### Machine Model (MM): legacy context

- Historically represented charged metal equipment with a low-impedance discharge.
- Appears in the legacy deck and some older literature.
- Do not assume correlation with HBM or CDM.
- Use the test model and revision required by the current product/customer specification.

*Source alignment: Analog Devices ESD glossary.*

### Charged Device Model (CDM)

- Device package becomes charged
- Device approaches grounded metal
- One pin makes first contact
- Very fast discharge leaves the device
- Local current density stresses internal structures

> **Decision takeaway:** Automation, trays, tubes and handlers can create CDM risk without a person touching the part.

*Source alignment: ESDA Fundamentals Part 1.*

### HBM, MM and CDM are not interchangeable

- **HBM:** Charged person → device; handling-oriented component model.
- **MM:** Legacy charged-machine representation; limited correlation.
- **CDM:** Charged device → ground; very fast package-dependent event.

*Source alignment: Analog Devices ESD glossary.*

### Catastrophic failure

- **Metal melt:** Current density damages interconnects.
- **Junction breakdown:** Semiconductor junction no longer meets specification.
- **Oxide rupture:** Thin dielectric is punctured.
- **Immediate detection:** Device may fail functional or parametric test.

*Source alignment: ESDA Fundamentals Part 1.*

### Latent and cumulative degradation

- A degraded device may still pass initial functional test.
- Leakage or margins can shift after an event.
- The latent-failure concept is debated; evidence must distinguish ESD from other overstress causes.
- Repeated mishandling can cumulatively degrade parameters.

*Source alignment: ESDA Fundamentals Part 1; Analog Devices.*

### ESD versus electrical overstress (EOS)

- ESD: rapid electrostatic charge transfer, usually short duration and fast rise time.
- Evidence includes handling history, field sources and microscopic damage pattern.
- EOS: broader excessive electrical energy exposure from power, wiring or transients.
- Do not label every burnt part as ESD without a disciplined failure analysis.

> **Decision takeaway:** Classification drives the right corrective action.

*Source alignment: ESDA Fundamentals Part 1.*

### Where exposure occurs

- Component manufacture
- Incoming inspection
- Assembly and test
- Packaging and logistics
- Installation and field service

*Source alignment: ESDA Fundamentals Part 1.*

### Which devices may be sensitive?

- **Semiconductors:** ICs, MOSFETs, diodes and precision analog parts.
- **Assemblies:** Populated PCBs and hybrid circuits.
- **Sensors:** Optoelectronic, microwave, piezoelectric and recording-head devices.
- **Supplier data:** Actual sensitivity comes from product qualification information.

*Source alignment: ESDA Fundamentals Part 1.*

### Economic impact pathway

- Undetected ESD exposure
- Yield loss or rework
- Escapes and field returns
- Warranty and investigation cost
- Customer trust and regulatory impact

> **Decision takeaway:** Prevention is usually cheaper than proving the origin of an intermittent failure.

*Source alignment: ESDA Fundamentals Part 1.*

### Risk-based prioritisation

- **Sensitivity:** Lowest credible device withstand level.
- **Exposure:** People, motion, insulators, automation and transport.
- **Detectability:** Whether damage is caught before shipment.
- **Consequence:** Safety, quality, cost, customer and downtime impact.

*Source alignment: ESDA Fundamentals Part 1.*

## Activity 1: Static Hazard Hunt at NovaSense Incoming Inspection

**Mapping:** K1 · A1  
**Objective:** Identify credible charge sources, exposed ESDS items, isolated conductors and field-coupling paths, then prioritise controls.

### Scenario

NovaSense receives MEMS sensor trays beside a label printer, stretch-wrap station and wheeled inspection trolley. Failure returns increased after a layout change, but no one has mapped charge-generation and induction risks.

### Detailed step-by-step procedure

1. Read the scenario and mark every ESDS item and handling handoff on the supplied floor sketch.
2. List each contact-and-separation event, material pair and motion that can generate charge.
3. Circle conductors that may be isolated from ground, including the trolley and metal fixtures.
4. Mark essential and non-essential insulators within the handling zone.
5. Trace one direct-contact discharge path and one field-induction path to a sensor tray.
6. Rate each hazard for sensitivity, exposure, detectability and consequence using the worksheet scale.
7. Select the top three risks and justify the ranking with observable evidence.
8. Propose one elimination, one grounding/bonding and one administrative control.
9. Define the measurement needed to confirm each proposed control.
10. Conduct a peer challenge: another group must identify one missed pathway or weak assumption.
11. Revise the map and record the change made after peer review.
12. Submit the completed hazard map, risk register and three-control proposal.

### Scenario questions

- Which hazard could damage a device without a visible spark?
- Which metal object could remain charged despite being conductive?
- What evidence would distinguish induction risk from direct contact?

### Evidence and acceptance

- **Evidence:** Annotated hazard map
- **Evidence:** Risk-prioritisation worksheet
- **Evidence:** Three-control proposal
- **Evidence:** Peer-review note
- [ ] At least eight credible hazards are identified
- [ ] Both direct and field-induced pathways are shown
- [ ] Top risks have evidence-based ratings
- [ ] Controls follow the ESD control hierarchy

Activity folder: `activities/activity-01-static-hazard-hunt-at-novasense-incoming-inspection/`

---

## Activity 2: Medical Microchip Failure Triage: ESD, EOS or Process Defect?

**Mapping:** K1 · A1  
**Objective:** Build an evidence-based hypothesis that separates HBM/CDM exposure, EOS and non-electrical process causes.

### Scenario

A medical-device ASIC passes wafer test but shows intermittent leakage after final assembly. A handler alarm occurred during the lot, yet the power-supply log also shows a transient. Management wants a defensible triage before quarantined product is released.

### Detailed step-by-step procedure

1. Review the event chronology, product symptoms, handler alarm and power-transient records.
2. Classify each clue as product, process, equipment, environmental or personnel evidence.
3. Describe the HBM and CDM mechanisms that could fit the handling sequence.
4. Describe the EOS mechanism that could fit the power record.
5. List at least two non-ESD alternatives that must remain open.
6. Create a comparison matrix of expected evidence for catastrophic, latent/cumulative and EOS damage.
7. Select immediate containment for the lot and neighbouring lots.
8. Specify non-destructive checks before destructive failure analysis.
9. Define the samples and controls required for a credible comparison.
10. State what result would support or weaken each hypothesis.
11. Prepare a five-minute management briefing that avoids claiming ESD without proof.
12. Record the next decision gate and authorised disposition options.

### Scenario questions

- Why is a monitor alarm not proof that this device was damaged by ESD?
- Which facts make CDM plausible?
- What would make the latent-failure claim weak?

### Evidence and acceptance

- **Evidence:** Chronology
- **Evidence:** Hypothesis matrix
- **Evidence:** Containment plan
- **Evidence:** Decision-gate briefing
- [ ] ESD, EOS and process alternatives remain explicit
- [ ] Evidence needed for each hypothesis is stated
- [ ] Containment protects product and evidence
- [ ] Conclusions use calibrated language

Activity folder: `activities/activity-02-medical-microchip-failure-triage-esd-eos-or-process-defect/`

---

## Module 2: ESD Control Principles, Equipment and Practices

**Mapping:** K1 · K3 · K4 · A1  
EPA design · grounding and bonding · personnel controls · ionisation · packaging · maintenance

### The ESD control hierarchy

- Identify ESDS items and process limits
- Remove unnecessary charge generators
- Ground and bond conductors
- Neutralise essential insulators
- Shield during storage and transport
- Verify and improve

> **Decision takeaway:** No single wrist strap is an ESD control programme.

*Source alignment: ESDA Fundamentals Part 1.*

### Electrostatic Protected Area (EPA)

- **Boundary:** A defined area with controlled entry and clear visual identification.
- **Common point:** A known reference for compatible grounding and bonding.
- **Approved items:** Only qualified materials, tools and equipment inside.
- **Behaviour:** Handling rules, training and compliance verification are enforced.

*Source alignment: ESDA Fundamentals Part 1.*

### Grounding versus bonding

- Grounding connects a conductor to a verified reference.
- Personnel and equipment paths must be compatible with safety requirements.
- Bonding connects conductors so they remain at substantially the same potential.
- Bond isolated metal objects even when they are not intentionally energised.

> **Decision takeaway:** The objective is equipotential handling—not simply attaching more wires.

*Source alignment: ESDA Fundamentals Part 1.*

### Common point ground architecture

- Facilities/equipment ground verified
- EPA common point established
- Mat and fixtures bonded
- Personnel grounding connected
- Continuity monitored and recorded

> **Decision takeaway:** Traceable paths make faults diagnosable.

*Source alignment: ESDA Fundamentals Part 1.*

### Personnel grounding choices

- **Seated work:** Wrist strap with tested cord and verified connection.
- **Standing/mobile:** Foot grounders or qualified footwear/flooring system.
- **Continuous monitoring:** Real-time alarm when the selected path leaves limits.

*Source alignment: ESDA Fundamentals Part 1.*

### Wrist-strap control loop

- Inspect band and cord
- Test before use
- Connect to approved point
- Maintain skin contact
- Respond immediately to alarm/failure

> **Decision takeaway:** A strap is effective only when the complete person–device–ground path works.

*Source alignment: ESDA Fundamentals Part 1.*

### Footwear and flooring as a system

- Foot grounders/ESD footwear provide the personnel interface.
- Correct wear and both-foot coverage matter.
- Qualified flooring completes the path.
- Contamination, wax, humidity and wear can change performance.

> **Decision takeaway:** Do not approve footwear independently of the floor and test method.

*Source alignment: ESDA Fundamentals Part 1.*

### Worksurface and tool control

- **Dissipative mat:** Provides controlled charge decay and a defined work zone.
- **Grounded fixtures:** Prevents isolated conductive metal.
- **ESD-safe tools:** Tweezers, brushes and dispensers selected for the process.
- **Housekeeping:** Cleaners and residues must not defeat electrical properties.

*Source alignment: ESDA Fundamentals Part 1.*

### Essential insulators

- Identify the process need
- Measure field at the actual use distance
- Increase separation where possible
- Apply ionisation or shielding
- Verify after changes

> **Decision takeaway:** Grounding an insulator does not remove its localised charge.

*Source alignment: ESDA Fundamentals Part 1.*

### Ionisation

- Balanced positive and negative ions neutralise charges on insulators and isolated conductors.
- Use where grounding is ineffective or impossible.
- Verify offset/balance and decay performance at the work location.
- Airflow, distance, contamination and emitter maintenance affect results.

> **Decision takeaway:** An ioniser supplements—not replaces—grounding.

*Source alignment: ESDA Fundamentals Part 1.*

### Electrostatic field shielding

- **Conductive enclosure:** Redistributes external charge and protects contents when closed.
- **Shielding bag:** Provides a protective envelope for transport outside the EPA.
- **Continuity:** Seams, closures and openings determine actual performance.

*Source alignment: ESDA Fundamentals Part 1.*

### Packaging functions are different

- **Low charging:** Limits triboelectric generation during contact/separation.
- **Dissipative:** Moves charge in a controlled way.
- **Conductive:** Rapidly redistributes charge; may need grounding.
- **Shielding:** Attenuates discharge current and electrostatic fields around contents.

*Source alignment: ESDA Fundamentals Part 1.*

### Handling ESDS items

- Confirm EPA readiness
- Ground the handler
- Open shielding package inside EPA
- Handle by body/edges
- Return to protective packaging before leaving

*Source alignment: Analog Devices; electrostatic-sensitive device overview.*

### Garments, gloves and finger cots

- Garments control charge from clothing and help contain personal items.
- Select design and grounding method for the process.
- Gloves/finger cots may support contamination control but are not automatically ESD-safe.
- Qualification and correct use are required.

> **Decision takeaway:** PPE appearance does not prove electrical performance.

*Source alignment: ESDA Fundamentals Part 1.*

### Carts, racks and material movement

- **Conductive wheels:** Maintain the intended path only when floor contact is suitable.
- **No loose insulators:** Remove ordinary plastic wrap and foam near exposed ESDS items.
- **Covered transport:** Use closed qualified containers outside EPA boundaries.
- **Route control:** Avoid high-charging areas and unmanaged handoffs.

*Source alignment: ESDA Fundamentals Part 1.*

### Maintenance is part of control

- Define owner and interval
- Inspect and clean
- Test with calibrated equipment
- Record result and disposition
- Trend failures and revise interval

> **Decision takeaway:** A control item without verification is an assumption.

*Source alignment: ESDA Fundamentals Part 1.*

### Common failure patterns

- **Disconnected strap:** Cord attached to an unverified point or worn over clothing.
- **Open bag:** Shielding package left open or folded incorrectly.
- **Insulator creep:** Tape, foam, trays or paperwork introduced without review.
- **Bad response:** Alarm bypassed, failed tester ignored or record completed retrospectively.

*Source alignment: ESDA Fundamentals Part 1.*

### Supervisor’s EPA readiness review

- **People:** Training current; grounding tested; behaviour observed.
- **Place:** Boundary, common point, floor, mat and ioniser verified.
- **Product:** Sensitivity known; packaging and process controls matched.

*Source alignment: ESDA Fundamentals Part 1.*

## Activity 3: Design and Commission an EPA for Orion Optics

**Mapping:** K3 · K4 · A1  
**Objective:** Design an EPA that controls people, place, product and process, then define commissioning evidence.

### Scenario

Orion Optics is moving laser-diode assembly into a small shared lab. The proposed bench has a mat and wrist strap but no documented boundary, common point, insulator policy or readiness test.

### Detailed step-by-step procedure

1. Define the ESDS items, process steps and product-sensitivity information required before design approval.
2. Draw the EPA boundary, entry point, product flow and locations of exposed handling.
3. Select the facility/equipment ground reference and show the common-point architecture.
4. Bond the mat, fixtures and other conductive objects on the diagram; flag unresolved isolated conductors.
5. Choose personnel grounding for seated and mobile work and define the pre-use response to failure.
6. Inventory essential/non-essential insulators and select removal, separation, shielding or ionisation controls.
7. Specify storage and transport packaging inside and outside the EPA.
8. Define signage, access, garments, tools and housekeeping requirements.
9. Create a commissioning test plan for ground continuity, worksurface, personnel grounding and ionisation.
10. Assign owners and record locations for qualification and verification evidence.
11. Run a red-team review using the checklist and close every critical gap.
12. Issue the EPA readiness certificate only when all acceptance criteria are met.

### Scenario questions

- What makes the area an EPA rather than simply a bench with a mat?
- Which item cannot be made safe by grounding alone?
- What evidence authorises production start?

### Evidence and acceptance

- **Evidence:** EPA layout
- **Evidence:** Grounding/bonding diagram
- **Evidence:** Insulator-control register
- **Evidence:** Commissioning plan and readiness certificate
- [ ] Boundary and product flow are unambiguous
- [ ] All conductors have a resolved status
- [ ] Essential insulators have controls
- [ ] Commissioning includes method, limit, owner and response

Activity folder: `activities/activity-03-design-and-commission-an-epa-for-orion-optics/`

---

## Activity 4: Select Controls for the Aster Robotics Handling Cell

**Mapping:** K3 · K4 · A1  
**Objective:** Match grounding, ionisation, shielding, handling and monitoring controls to both human and automated exposure pathways.

### Scenario

A robot transfers packaged ICs from plastic tubes to a grounded nest. Operators also perform manual rework. The team proposes more wrist straps, but field readings near the tube exit remain high.

### Detailed step-by-step procedure

1. Map every charged-person, charged-device and charged-machine pathway through the cell.
2. Identify where grounding is effective and where it is ineffective because the material is insulating.
3. Select personnel grounding for normal operation, setup and manual rework.
4. Select bonding and ground monitoring for robot fixtures, nests, tools and carts.
5. Evaluate whether the plastic tubes are essential and document the decision.
6. Define ioniser type, placement, airflow constraints and the required work-position checks.
7. Choose packaging/transfer methods that preserve shielding until entry into the protected process.
8. Define alarms, interlocks or stop conditions for loss of ground or ionisation.
9. Create a preventive-maintenance plan with cleaning and verification intervals.
10. Prepare a control-selection matrix linking each risk to control, owner, evidence and residual risk.
11. Walk through a changeover and maintenance intervention to find temporary exposures.
12. Present the selected design and respond to a cost-versus-risk challenge from management.

### Scenario questions

- Why will adding wrist straps not solve the tube-exit field?
- Which controls address CDM risk?
- What should happen when an ioniser check fails?

### Evidence and acceptance

- **Evidence:** Exposure-path map
- **Evidence:** Control-selection matrix
- **Evidence:** Monitoring/stop-condition plan
- **Evidence:** Maintenance plan
- [ ] Controls cover human and automated pathways
- [ ] Insulators are addressed by an appropriate method
- [ ] Monitoring has explicit response actions
- [ ] Residual risk is stated

Activity folder: `activities/activity-04-select-controls-for-the-aster-robotics-handling-cell/`

---

## Module 3: ESD Standards, Testing and Auditing

**Mapping:** K2 · K3 · A2 · A3  
Control programme structure · measurements · compliance verification · evidence · performance metrics

### Standards define a control system

- ANSI/ESD S20.20 and IEC 61340-5-1 structure organisational controls for protecting ESDS items.
- Use the current controlled copy, customer requirements and product sensitivity data for exact limits and methods.

> **Decision takeaway:** Training slides are not a substitute for the purchased/current standard.

*Source alignment: ESDA Fundamentals Part 1.*

### Control programme architecture

- Scope and responsibilities
- Technical requirements
- Product qualification
- Compliance verification
- Records, corrective action and management review

*Source alignment: EOS/ESD Association.*

### Product qualification versus compliance verification

- Qualification demonstrates that an ESD control item/type is capable of meeting specified requirements.
- Evidence may include supplier data or internal testing.
- Compliance verification checks that installed controls remain effective in routine use.
- It uses defined methods, frequencies, limits and response actions.

> **Decision takeaway:** Buying a qualified item does not eliminate ongoing checks.

*Source alignment: ESDA Fundamentals Part 1.*

### Instrument-to-risk map

- **Resistance meter:** Worksurfaces, floors, garments, packaging and ground paths.
- **Personnel tester:** Wrist straps, footwear and person/footwear/floor systems.
- **Field meter:** Electrostatic field and charged-object screening.
- **Charge plate monitor:** Ioniser decay and offset/balance performance.

*Source alignment: ESDA Fundamentals Part 1.*

### Measurement discipline

- Define method and limit
- Confirm calibration/status
- Condition sample/environment
- Measure at specified points
- Record result and uncertainty/context
- Act on failure

> **Decision takeaway:** A number without method, units and conditions is weak evidence.

*Source alignment: ESDA Fundamentals Part 1.*

### Wrist strap and footwear checks

- Daily/user checks screen the assembled personal grounding path before work.
- Failure requires immediate stop, retest and disposition.
- Periodic technical checks verify components, testers and flooring systems.
- Trend repeated failures by user, device, location and shift.

> **Decision takeaway:** Do not pre-fill a log or accept an unexplained retest pass.

*Source alignment: ESDA Fundamentals Part 1.*

### Surface and point-to-ground resistance

- **Point-to-point:** Characterises the path across a surface/material.
- **Point-to-ground:** Characterises the installed path to the designated ground.
- **Context:** Electrodes, voltage, dwell, humidity and cleanliness influence the reading.

*Source alignment: ESDA Fundamentals Part 1.*

### Ioniser performance checks

- Inspect placement and airflow
- Warm up per procedure
- Measure positive/negative decay
- Measure offset/balance
- Clean or adjust
- Repeat and record

> **Decision takeaway:** Test at the product work position—not only next to the ioniser.

*Source alignment: ESDA Fundamentals Part 1.*

### Audit evidence pyramid

- **Observe:** Actual behaviour at the workstation.
- **Measure:** Current test results from calibrated instruments.
- **Interview:** Personnel can explain risk and response.
- **Records:** Training, qualification, maintenance, failures and CAPA are traceable.

*Source alignment: ESDA Fundamentals Part 1.*

### Risk-based audit sampling

- Increase attention where products are most sensitive, exposure is high or process changes are recent.
- Sample across shifts, people and workstations.
- Do not let a checklist replace observation and measurement.
- A single passing sample does not prove the entire system.

> **Decision takeaway:** Sampling rationale belongs in the audit record.

*Source alignment: ESDA Fundamentals Part 1.*

### Nonconformity grading

- **Critical:** Immediate product/safety exposure; contain and escalate.
- **Major:** Systemic or repeated breakdown; formal CAPA and verification.
- **Minor/observation:** Local weakness or improvement opportunity; track proportionately.

*Source alignment: ESDA Fundamentals Part 1.*

### Corrective-action loop

- Contain affected product/process
- Define problem with evidence
- Analyse root and contributing causes
- Implement corrective/preventive actions
- Verify effectiveness
- Standardise and close

> **Decision takeaway:** Closure requires effectiveness evidence—not merely an action-completed date.

*Source alignment: ESDA Fundamentals Part 1.*

### Useful ESD performance metrics

- **Leading:** Test completion, first-pass pass rate, overdue calibration, training currency.
- **Process:** EPA audit score, insulator findings, alarm response time.
- **Lagging:** ESD-attributed escapes, scrap, rework and field returns.
- **Learning:** Repeat causes, CAPA recurrence and time-to-effective closure.

*Source alignment: ESDA Fundamentals Part 1.*

### Management review questions

- **Effective?:** Are controls reducing exposure and failures?
- **Adequate?:** Do changes in products/processes require new controls?
- **Sustained?:** Are verification, training and CAPA completed on time?

*Source alignment: ESDA Fundamentals Part 1.*

## Activity 5: Execute a Compliance Verification Round

**Mapping:** K2 · K3 · A2  
**Objective:** Plan, execute and record traceable checks for personnel grounding, resistance, electrostatic field and ioniser performance.

### Scenario

Meridian Electronics has four EPAs on two shifts. Recent records show perfect results but several tester failures were repaired without documented product disposition. You must execute a verification round using a simulated data pack.

### Detailed step-by-step procedure

1. Confirm the verification procedure, current limits and sampling plan from the controlled programme documents.
2. Check each instrument identity, calibration status, battery/zero check and suitable accessories.
3. Record temperature, relative humidity, area, shift and relevant process condition.
4. Review daily wrist-strap and footwear test records for completeness, first-pass failures and response actions.
5. Use the simulated readings to evaluate person/footwear/floor and wrist-strap results.
6. Evaluate point-to-point and point-to-ground resistance readings with method and electrode details.
7. Evaluate field readings at the stated work distance and identify uncontrolled essential insulators.
8. Evaluate positive/negative decay and offset/balance readings at the work position.
9. Classify each result as conforming, nonconforming or insufficient evidence.
10. For every failure, define immediate containment, retest rules, product impact review and escalation.
11. Calculate first-pass pass rate and overdue-check rate; explain what each metric can and cannot prove.
12. Sign the evidence package and retain raw data, calculations and disposition decisions.

### Scenario questions

- Why is a retest pass insufficient without investigating the first failure?
- Which contextual data makes a resistance reading defensible?
- Where should ioniser performance be checked?

### Evidence and acceptance

- **Evidence:** Completed measurement log
- **Evidence:** Failure/disposition records
- **Evidence:** Metric calculation
- **Evidence:** Signed evidence package
- [ ] Every result includes method, units and conditions
- [ ] Instrument status is verified
- [ ] First-pass failures remain visible
- [ ] Product impact and response are documented

Activity folder: `activities/activity-05-execute-a-compliance-verification-round/`

---

## Activity 6: Standards-Based EPA Audit at Helix Assembly

**Mapping:** K2 · A2 · A3  
**Objective:** Conduct a risk-based audit using observation, measurement, interview and records, then issue graded findings and corrective-action requests.

### Scenario

Helix Assembly claims alignment to ANSI/ESD S20.20 and IEC 61340-5-1. A new customer requests evidence that controls are implemented, verified and improved—not merely purchased.

### Detailed step-by-step procedure

1. Confirm audit scope, criteria, process boundaries, product sensitivity and previous findings.
2. Build a sampling plan across shifts, workstations, products and recent changes.
3. Review the ESD control programme, roles, qualification evidence and compliance-verification plan.
4. Observe EPA entry, grounding, handling, packaging and response to simulated alarms.
5. Interview an operator, technician and manager using role-specific competence questions.
6. Review current measurement, calibration, maintenance, training and change-control records.
7. Trace one ESDS lot from receipt through assembly, test, storage and dispatch.
8. Triangulate each potential finding with at least two evidence types where practical.
9. Grade findings by exposure and system impact; define immediate containment where required.
10. Write each finding with requirement/criterion, objective evidence, gap and risk.
11. Agree owners and target dates without allowing the auditee to close findings during the meeting.
12. Define follow-up evidence and effectiveness checks, then issue the audit report.

### Scenario questions

- What evidence shows a control is sustained rather than merely installed?
- Why must the exact controlled standard govern numerical limits?
- What makes a finding actionable?

### Evidence and acceptance

- **Evidence:** Audit plan
- **Evidence:** Completed checklist
- **Evidence:** Evidence register
- **Evidence:** Graded findings and follow-up plan
- [ ] Sampling is risk-based
- [ ] Findings cite objective evidence
- [ ] Critical exposure triggers containment
- [ ] Follow-up tests effectiveness, not only completion

Activity folder: `activities/activity-06-standards-based-epa-audit-at-helix-assembly/`

---

## Module 4: Training, Awareness and Incident Improvement

**Mapping:** K4 · A2 · A3  
Competence · behaviour · reporting · root-cause analysis · CAPA · management ownership

### Competence is role-specific

- **Operators:** Recognise ESDS items, enter EPA correctly and handle/pack safely.
- **Technicians:** Set up, test, troubleshoot and maintain controls.
- **Engineers:** Define limits, qualify controls and investigate events.
- **Managers:** Provide resources, review metrics and remove systemic barriers.

*Source alignment: ESDA Fundamentals Part 1.*

### From awareness to reliable behaviour

- Explain the invisible risk
- Demonstrate the correct method
- Practise with feedback
- Observe on the job
- Reinforce and requalify

> **Decision takeaway:** A signature on attendance is not evidence of competence.

*Source alignment: ESDA Fundamentals Part 1.*

### ESD champions and supervision

- **Coach:** Give immediate, specific feedback at the workstation.
- **Escalate:** Stop unsafe handling and trigger containment when required.
- **Learn:** Share incident lessons without normalising blame.

*Source alignment: ESDA Fundamentals Part 1.*

### Recognising a possible ESD incident

- **Product symptom:** Sudden failure, parametric shift, intermittent behaviour or unexplained fallout.
- **Control signal:** Monitor alarm, failed tester, ioniser drift or broken ground path.
- **Exposure clue:** Unprotected handling, ordinary plastic, low humidity or process change.
- **Caution:** Symptoms are not proof; preserve evidence for diagnosis.

*Source alignment: ESDA Fundamentals Part 1.*

### Immediate response

- Stop and protect the process
- Segregate potentially affected product
- Preserve settings, logs and samples
- Notify defined roles
- Begin evidence-based triage

> **Decision takeaway:** Do not reset equipment or discard suspect parts before evidence capture.

*Source alignment: ESDA Fundamentals Part 1.*

### Incident evidence set

- **What/where/when:** Product, lot, station, timestamp and sequence.
- **Environment:** Humidity, temperature, nearby motion and insulators.
- **Controls:** Tester logs, monitor alarms, grounding and ioniser status.
- **People/process:** Who handled it, procedure used and recent changes.

*Source alignment: ESDA Fundamentals Part 1.*

### Root-cause analysis without blame

- Ask why the system allowed exposure: design, maintenance, method, material, measurement or management.
- Distinguish root, contributing and detection causes.
- Avoid stopping at 'operator error'.
- A repeated behaviour usually reflects unclear standards, weak design, workload or ineffective supervision.

> **Decision takeaway:** Correct the system that shaped the behaviour.

*Source alignment: ESDA Fundamentals Part 1.*

### Selecting corrective actions

- Remove generator/exposure
- Engineer a reliable ground or enclosure
- Add detection/monitoring
- Standardise work and response
- Train and verify competence
- Measure sustained effectiveness

> **Decision takeaway:** Prefer controls that do not rely solely on memory.

*Source alignment: ESDA Fundamentals Part 1.*

### Communicating ESD risk

- **Frontline:** Show the exact handling risk and the stop-work response.
- **Engineering:** Use measurements, failure evidence and process capability.
- **Management:** Translate risk into yield, customer, compliance and continuity impact.

*Source alignment: ESDA Fundamentals Part 1.*

### A sustainable ESD culture

- **Visible ownership:** Named programme coordinator and local owners.
- **Just reporting:** Near misses and failures can be reported without concealment.
- **Closed loop:** Findings become actions, verified changes and updated standards.
- **Learning cadence:** Metrics, incidents and changes are reviewed regularly.

*Source alignment: ESDA Fundamentals Part 1.*

### Competency certification

- Internal authorisation should match the tasks a person performs.
- Use knowledge, demonstration and observed-work evidence.
- External credentials may support development but do not replace site-specific qualification.
- Reassess after major changes, lapse or repeated nonconformance.

> **Decision takeaway:** Competence must remain current at the point of work.

*Source alignment: ESDA Fundamentals Part 1.*

## Activity 7: Investigate the PulseMed ESD Incident

**Mapping:** K4 · A2 · A3  
**Objective:** Contain risk, preserve evidence, identify system causes and produce a verified CAPA plan.

### Scenario

PulseMed sees intermittent failures in a safety-relevant control board after a temporary operator used ordinary bubble wrap near final test. A monitor alarm was acknowledged but production continued for 47 minutes.

### Detailed step-by-step procedure

1. Initiate stop-work and quarantine product handled during the exposure window.
2. Preserve monitor logs, tester results, packaging samples, workstation state and operator accounts.
3. Create a verified timeline from the first process change to containment.
4. Define the problem using product, place, time, extent and observed symptoms without assuming causation.
5. Map direct, induction and CDM exposure pathways created by the bubble wrap and handling sequence.
6. Use a fishbone and five-whys analysis across method, material, machine, measurement, people and management.
7. Identify root, contributing and detection causes; avoid ending at 'operator error'.
8. Select immediate correction, systemic corrective action and preventive action for similar areas.
9. Define affected-product disposition and the technical evidence required for release or scrap.
10. Assign CAPA owners, dates, resources and leading indicators.
11. Define an effectiveness review after implementation, including observation, field measurement and recurrence checks.
12. Prepare a factual incident report and a psychologically safe learning briefing.

### Scenario questions

- Which system weakness allowed the alarm to be ignored?
- What evidence must be preserved before resetting the workstation?
- How will you prove the CAPA was effective?

### Evidence and acceptance

- **Evidence:** Containment record
- **Evidence:** Timeline and causal analysis
- **Evidence:** CAPA plan
- **Evidence:** Effectiveness-verification plan
- [ ] Exposure window and product scope are defined
- [ ] Causes extend beyond individual blame
- [ ] Actions address root and detection causes
- [ ] Effectiveness has measurable evidence

Activity folder: `activities/activity-07-investigate-the-pulsemed-esd-incident/`

---

## Activity 8: Management Capstone: Build the Apex ESD Control Plan

**Mapping:** K1–K4 · A1–A3  
**Objective:** Integrate the complete course into a management-ready ESD control plan and defend it under assessment-style questioning.

### Scenario

Apex Microsystems is opening a mixed lab/factory line for sensitive industrial controllers. Management needs an auditable ESD control plan before customer qualification, covering controls, verification, competence, incidents and improvement.

### Detailed step-by-step procedure

1. Define scope, ESDS products, process boundaries, applicable customer/standard criteria and programme objectives.
2. Assign programme coordinator, technical owners, area owners, operators and management-review responsibilities.
3. Create the process risk map and select controls using elimination, grounding/bonding, ionisation, shielding and administrative layers.
4. Define EPA requirements for people, workstation, equipment, materials, packaging, logistics and field service.
5. Build the qualification register for each control item and required evidence.
6. Build the compliance-verification matrix with item, method, limit/source, frequency, owner, record and response.
7. Create the role-based training and competency matrix with initial, observed and refresher evidence.
8. Define incident reporting, containment, investigation, CAPA and effectiveness verification.
9. Select leading, process, lagging and learning metrics with targets and review frequency.
10. Run a tabletop scenario for a failed personnel tester and an ioniser drift; trace every decision and record.
11. Conduct a customer-assessor challenge using the two Case Study task prompts.
12. Revise, approve and issue the plan with a 90-day implementation roadmap.

### Scenario questions

- How does the plan demonstrate A1, A2 and A3?
- Which records prove the control programme remains effective?
- What management decision is triggered by deteriorating leading indicators?

### Evidence and acceptance

- **Evidence:** ESD control plan
- **Evidence:** Qualification and verification matrices
- **Evidence:** Competency matrix
- **Evidence:** Metrics dashboard and 90-day roadmap
- [ ] All K and A criteria are traceable
- [ ] Controls have owners and evidence
- [ ] Failure response and CAPA are closed-loop
- [ ] Plan uses current controlled standards for exact requirements

Activity folder: `activities/activity-08-management-capstone-build-the-apex-esd-control-plan/`

---

## Reference sources

- [Course page](https://www.tertiarycourses.com.sg/wsq-electrostatic-discharge-esd-control-for-lab-and-factory-engineers-and-managers.html)
- [Electrostatic discharge overview](https://en.wikipedia.org/wiki/Electrostatic_discharge)
- [Analog Devices ESD glossary](https://www.analog.com/en/resources/glossary/esd.html)
- [EOS/ESD Association Fundamentals Part 1](https://www.esda.org/esd-overview/esd-fundamentals/part-1-an-introduction-to-esd/)
- [Creative Safety Supply ESD explainer](https://www.creativesafetysupply.com/qa/electrical-safety/what-does-esd-stand-for)
- [Toshiba ESD FAQ](https://toshiba.semicon-storage.com/ap-en/semiconductor/knowledge/faq/diode_tvs-diodes/what-is-electrostatic-discharge-esd.html)
- [Electrostatic-sensitive device overview](https://en.wikipedia.org/wiki/Electrostatic-sensitive_device)
- [EOS/ESD Association](https://www.esda.org/)
- [Schneider Electric community ESD discussion](https://community.se.com/t5/Industry-Automation-and-Control/What-is-an-ESD/td-p/237728)
- [ESD disambiguation](https://en.wikipedia.org/wiki/ESD)
